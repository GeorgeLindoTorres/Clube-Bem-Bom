<template>
    <section class="secao-busca container center">
          <div class="busca-junta-lupa-texto">
          <img type="button" src="../../assets/img/search-icon.svg" class="lupa-busca" alt="lupa">
          <input class="campo-busca" v-on:input="filtro = $event.target.value" name="busca-principal" id="busca-principal" placeholder=" Pesquisar...">          
          </div>
          <vue-dropdown class="botao-segmentos" textColor="white" :config="config"></vue-dropdown>
    </Section>  
</template>

<script>
import VueDropdown from 'vue-dynamic-dropdown'
export default {
    components: {
  VueDropdown
},
data: function() {
    return {
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
                return this.parceiros.filter(parceiro => exp.test(paceiro.nome))
            } else {
                return this.parceiros
            }
        }

    }
}
</script>

<style>
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

