<template>
 <section class="sessao-parceiros">
     <div class="parceiros">
            <div class="container center">
            <h1 class="texto-chamada-parceiros">Muitas <span class="detalhe-chamada-parceiros">vantagens</span> e <span class="detalhe-chamada-parceiros">descontos</span> exclusivos</h1>
            </div>
     </div>
     <card-parcerio></card-parcerio>
     <card-parcerio></card-parcerio>
    </section>
</template>

<script>
import CardParceiro from '../card-parceiro/CardParceiro.vue'
export default {
    components: {
        'card-parcerio': CardParceiro
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
  padding-top: 1rem;
  font-family: system-ui;
  font-style: italic;
  font-weight: bold;
  font-size: 28px;
  line-height: 29px;
  text-align: center;
  color: #000000;
    padding-bottom: 2rem;
}

.detalhe-chamada-parceiros {
  color: #209532;
}

.center {
  text-align: center;
}
</style>