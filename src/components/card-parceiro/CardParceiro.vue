<template>
  <section id="card-parceiros" class="flex">
    <div class="card card-convenio">
      <img :src="imagem" class="card-img-top" alt="..." />
      <div class="card-body">
        <h5 class="nome-parceiro-card">{{ nome }}</h5>
        <p class="texto-beneficio-card">{{ beneficio }}</p>
        <vsa-list class="btn-utilizar">
          <vsa-item>
            <vsa-heading> COMO UTILIZAR </vsa-heading>

            <vsa-content>
              <div class="texto-beneficio">
                <p>{{ comoUtiliza }}</p>
                <p>Contato: {{ contato }}</p>
                <p>Telefone: {{ telefone }}</p>
                <p>Endereço: {{ endereco }}</p>
              </div>
            </vsa-content>
          </vsa-item>
        </vsa-list>
        <div class="btn btn-contato">
          <a class="btn-contato-link" :href="whatsapp"
            ><img
              src="src\assets\img\call-icon.svg"
              class="call-icon"
            />contato</a
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { VsaList, VsaItem, VsaHeading, VsaContent } from "vue-simple-accordion";
import "vue-simple-accordion/dist/vue-simple-accordion.css";
export default {
  components: {
    VsaList,
    VsaItem,
    VsaHeading,
    VsaContent,
  },
  props: ['imagem','nome','beneficio','comoUtiliza','contato','telefone','endereco','whatsapp']
};
</script>

<style>
.vsa-item__content {
  background-color: white;
}
.vsa-item__trigger:focus,
.vsa-item__trigger:hover {
  outline: none;
  background-color: #005caa;
  color: #ffffff;
}
.btn-utilizar {
  --vsa-heading-padding: 0.75rem 0.75rem;
  --vsa-max-width: 720px;
  --vsa-min-width: none;
  --vsa-bg-color: #005caa;
  --vsa-text-color: white;
  --vsa-highlight-color: #fff;
  color: black;
  border-radius: 0.25rem;
  text-align: center;
}
.flex {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.center {
  text-align: center;
}
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
  background-color: #fff;
  background-clip: border-box;
  border: 1px solid rgba(0, 0, 0, 0.125);
  border-radius: 0.25rem;
}
.card-convenio {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  width: 18rem;
  margin-top: 2rem;
}

.card-body {
  flex: 1 1 auto;
  padding: 1rem 1rem;
  text-align: left;
}

.call-icon {
  width: 16px;
  margin-right: 9px;
}

.nome-parceiro-card {
  margin-bottom: 0.5rem;
  font-style: normal;
  font-weight: 500;
  font-size: 22px;
  line-height: 25px;
  color: #000000;
}
.texto-beneficio {
  margin-bottom: 1rem;
  font-weight: 300;
  font-size: 20px;
  line-height: 23px;
  color: #000000;
}
.texto-beneficio p {
  padding: 0.5rem;
  text-align: left;
  font-family: sans-serif;
  font-size: 16px;
  line-height: 1.5;
}
.texto-beneficio-card {
  margin-bottom: 1rem;
  font-style: italic;
  font-weight: 300;
  font-size: 20px;
  line-height: 23px;
  color: #000000;
}

.btn-como-utilizar {
  cursor: pointer;
  width: 100%;
  background: #005caa;
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 21px;
  text-align: center;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
  color: #ffffff;
  border: 1px solid transparent;
  padding: 0.375rem 0.75rem;
  border-radius: 0.25rem;
  text-align: center;
}

.btn-contato {
    cursor: pointer;
  margin-top: 0.5rem;
  width: 100%;
  background: #209532;
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 21px;
  text-align: center;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
  border: 1px solid transparent;
  padding: 0.75rem 0;
  border-radius: 0.25rem;
}
.btn-contato-link {
  color: #ffffff;
  text-decoration: none;
}

.btn-contato:hover {
  color: #ffffff;
}

.vsa-item__trigger__content {
  font-weight: 600;
  font-size: 1.2rem;
}
.vsa-item__heading,
.vsa-item__trigger {
  display: inline;
}
</style>