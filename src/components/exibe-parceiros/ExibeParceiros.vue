<template>
<div> 
<section class="secao-busca container center">
          <div class="busca-junta-lupa-texto">
          <img type="button" src="../../assets/img/search-icon.svg" class="lupa-busca" alt="lupa">
          <input class="campo-busca" v-on:input="filtro = $event.target.value" name="busca-principal" id="busca-principal" placeholder=" Pesquisar...">          
          </div>          
          <vue-dropdown class="botao-segmentos" textColor="white" :config="config"></vue-dropdown>
    </Section>      
 <section class="sessao-parceiros">
     <div class="parceiros">
            <div class="container center">
            <h1 class="texto-chamada-parceiros">Muitas <span class="detalhe-chamada-parceiros">vantagens</span> e <span class="detalhe-chamada-parceiros">descontos</span> exclusivos</h1>
            </div>
     </div>
     <ul>
       <li v-for="parceiro of parceirosComFiltro">
     <card-parceiro :imagem="parceiro.imagem" :nome="parceiro.nome" :beneficio="parceiro.beneficio" :comoUtiliza="parceiro.comoUtiliza" :contato="parceiro.contato" :telefone="parceiro.telefone" :endereco="parceiro.endereco" :whatsapp="parceiro.whatsapp"></card-parceiro>
       </li>
     </ul>     
    </section>
</div>    
</template>

<script>
import CardParceiro from '../card-parceiro/CardParceiro.vue'
import VueDropdown from 'vue-dynamic-dropdown'
export default {    
    components: {
        'card-parceiro': CardParceiro,
        VueDropdown
    },    
  data() {
    return{
      parceiros:[],
      filtro: "",
        config: {
            options: [
                {
                    value: "Educação"
                },
                {
                    value: "Lazer"
                },
                {
                    value: "Serviços"
                },
                {
                    value: "Saúde e Beleza"
                },                
            ],
            prefix: "Buscar por segmento",
            backgroundColor: "#005caa",
            backgroundExpandedColor: "white",
        }
    }
  },
  computed: {
        parceirosComFiltro() {
            if(this.filtro) {
              let exp = new RegExp(this.filtro.trim(), 'i');
              return this.parceiros.filter(parceiro => exp.test(parceiro.nome))
            } else {
                return this.parceiros
            }
        }
  },  
  created() {
    this.$http.get('http://localhost:3000/v1/parceiros')
      .then(res => res.json())
      .then(parceiros => this.parceiros = parceiros, err => console.log(err));
  }  
};
</script>

<style>
.sessao-parceiros {
  margin-top: 1rem;
  background: #e5e5e5;
  width: 100%;
  height: 100%;
}

.texto-chamada-parceiros {
  padding: 1rem 0 0.25rem 0;
  font-family: system-ui;
  font-style: italic;
  font-weight: bold;
  font-size: 28px;
  line-height: 29px;
  text-align: center;
  color: #000000;
}

.detalhe-chamada-parceiros {
  color: #209532;
}

.center {
  text-align: center;
}
.busca-junta-lupa-texto{
    display: flex;
}

.lupa-busca{
    padding-left: 10px;
    padding-right: 6px;
    box-shadow: -1px 2px 1px 1px rgb(0 0 0 / 10%);
    border-radius: 9px 0 0 9px;
    border: none;
    margin-bottom: 1rem;
}

.campo-busca{
    width: 100%;
    box-shadow: 1px 2px 1px 1px rgb(0 0 0 / 10%);
    border-radius: 0 9px 9px 0;
    border: none;
    height: 40px;
    margin-bottom: 1rem;
}

.botao-segmentos{
    margin-bottom: 1rem;
}
</style>