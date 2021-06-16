<template>
 <section class="sessao-parceiros">
     <div class="parceiros">
            <div class="container center">
            <h1 class="texto-chamada-parceiros">Muitas <span class="detalhe-chamada-parceiros">vantagens</span> e <span class="detalhe-chamada-parceiros">descontos</span> exclusivos</h1>
            </div>
     </div>
     <ul>
       <li v-for="parceiro of parceiros">
     <card-parceiro :imagem="parceiro.imagem" :nome="parceiro.nome" :beneficio="parceiro.beneficio" :comoUtiliza="parceiro.comoUtiliza" :contato="parceiro.contato" :telefone="parceiro.telefone" :endereco="parceiro.endereco" :whatsapp="parceiro.whatsapp"></card-parceiro>
       </li>
     </ul>     
    </section>
</template>

<script>
import CardParceiro from '../card-parceiro/CardParceiro.vue'
export default {
    components: {
        'card-parceiro': CardParceiro
    },
  data() {
    return{
      parceiros:[],
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
</style>