<template>
        <section id="card-parceiros" class="flex">
            <div class="card card-convenio">
              <img src="data:image/jpeg;base64,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" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="nome-parceiro-card">Facens</h5>
                <p class="texto-beneficio-card">Até 20% de desconto*</p>
                <vsa-list class="btn-utilizar">
            <!-- Here you can use v-for to loop through items  -->
                                <vsa-item>
                                <vsa-heading>
                                    COMO UTILIZAR
                                </vsa-heading>

                                <vsa-content>
                                  <div class="texto-beneficio">
                                    <p>Apresente o seu holerite e/ou o cartão de associado do clube no ato da matrícula.
                                    Benefícios do convênio:</p>
                                      <p>- 10 % de desconto na graduação.</p>
                                      <p> - 20% de desconto na Pós.</p>
                                      <p> Contato: Pamela </p>
                                      <p> Telefone: 15 3346-1220 </p>
                                      <p> Endereço: Rodovia Senador José Ermírio de Moraes, 1425 - Jardim Constantino Matucci, Sorocaba - SP, 18085-784</p>
                                  </div>
                                </vsa-content>
                            </vsa-item>
                        </vsa-list>              
                        <div class="btn btn-contato"> 
                          <a class="btn-contato-link" href="https://api.whatsapp.com/send?phone=5515991043885"><img src="src\assets\img\call-icon.svg" class="call-icon">contato</a>
                        </div>
                  </div>
                </div>                
        </section>
</template>

<script>
import {
  VsaList,
  VsaItem,
  VsaHeading,
  VsaContent,
  
} from 'vue-simple-accordion';
import 'vue-simple-accordion/dist/vue-simple-accordion.css';
export default {
    components: {
    VsaList,
    VsaItem,
    VsaHeading,
    VsaContent,
    
  }
}
</script>

<style>
.vsa-item__content {
    background-color: white;
}
.btn-utilizar{
      --vsa-max-width: 720px;
      --vsa-min-width: none;
      --vsa-bg-color: #005caa;
      --vsa-text-color: white;
      --vsa-highlight-color: #fff;      
      color: black;
      border-radius: .25rem;
}
.flex{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}
.center{
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
    border: 1px solid rgba(0,0,0,.125);
    border-radius: .25rem;
}
.card-convenio{
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    width: 18rem;
    margin-top: 2rem;
}

.card-body{
    flex: 1 1 auto;
    padding: 1rem 1rem;
    text-align: left; 
}

.call-icon{
    width: 16px;
    margin-right: 3px;
    
}

.nome-parceiro-card{
    margin-bottom: .5rem;
    font-style: normal;
    font-weight: 500;
    font-size: 22px;
    line-height: 25px;
    color: #000000;
}
.texto-beneficio{
   margin-bottom: 1rem;    
   font-weight: 300;
   font-size: 20px;
   line-height: 23px;   
   color: #000000;
}
.texto-beneficio p {
  padding: .5rem;
}
.texto-beneficio-card{
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
    background: #005CAA;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    text-align: center;
    text-transform: uppercase;
    margin-bottom: .5rem;
    color: #FFFFFF;
    border: 1px solid transparent;
    padding: .375rem .75rem;
    border-radius: .25rem;
}

.btn-contato{
    margin-top: .5rem;
    width: 100%;
    background: #209532;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    text-align: center;
    text-transform: uppercase;
    margin-bottom: .5rem;
    border: 1px solid transparent;
    padding: .75rem 0;
    border-radius: .25rem;
}
.btn-contato-link{
    color: #FFFFFF;
    text-decoration: none;
}

.btn-contato:hover{
    color: #FFFFFF;
}

.vsa-item__trigger__content {
    font-weight: 600;
    font-size: 1rem;
}
</style>