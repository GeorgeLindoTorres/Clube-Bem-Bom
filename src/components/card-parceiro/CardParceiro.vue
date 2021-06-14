<template>
        <section id="card-parceiros" class="flex">
            <div class="card card-convenio">
              <img src="https://www.facens.br/system/posts/images/000/001/106/display/WhatsApp_Image_2018-12-05_at_16.53.42.jpeg?1544187036" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="nome-parceiro-card">Facens</h5>
                <p class="texto-beneficio-card">Até 20% de desconto*</p>
                <div class="accordion" id="accordionExample">
                  <div class="accordion-item">
                    <h2 class="accordion-header" id="headingOne">
                      <button class="btn btn-como-utilizar" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                        Como Utilizar
                      </button>
                        </h2>
                        <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne" data-bs-parent="#accordionExample">
                          <div class="accordion-body">
                            <p>Apresente o seu holerite e/ou o cartão de associado do clube no ato da matrícula.
                            Benefícios do convênio:</p>
                              <p>- 10 % de desconto na graduação.</p>
                              <p> - 20% de desconto na Pós.</p>
                              <p> Contato: Pamela </p>
                              <p> Telefone: 15 3346-1220 </p>
                              <p> Endereço: Rodovia Senador José Ermírio de Moraes, 1425 - Jardim Constantino Matucci, Sorocaba - SP, 18085-784</p>
                          </div>
                        </div>
                      </div>
                      </div>
                    <a href="https://api.whatsapp.com/send?phone=5515991043885" class="btn btn-contato"><img src="img/call-icon.svg" class="call-icon"> contato</a>
                  </div>
                </div>
        </section>
</template>

<script>
export default {

}
</script>

<style>
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
    text-align: left; 
}

.call-icon{
    width: 16px;
    margin-right: 3px;
    
}

.nome-parceiro-card{
    
    font-style: normal;
    font-weight: 500;
    font-size: 22px;
    line-height: 25px;
    color: #000000;
}

.texto-beneficio-card{
    
    font-style: italic;
    font-weight: 300;
    font-size: 20px;
    line-height: 23px;   
    color: #000000;
}

.btn-como-utilizar{
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
}

.btn-contato{
    margin-top: .5rem;
    width: 100%;
    background: #209532;
    font-family: Ubuntu;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    text-align: center;
    text-transform: uppercase;
    margin-bottom: .5rem;
    color: #FFFFFF;
    border-color: none;
}

.btn-contato:hover{
    color: #FFFFFF;
}
</style>