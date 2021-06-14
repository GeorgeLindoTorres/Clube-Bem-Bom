<template>
    <section class="secao-busca container center">
          <div class="busca-junta-lupa-texto">
          <img type="button" src="../../assets/img/search-icon.svg" class="lupa-busca" alt="lupa">
          <input class="campo-busca" name="busca-principal" id="busca-principal" placeholder=" Pesquisar...">
          </div>

          <div class="dropdown">
            <button class="btn btn-secondary dropdown-toggle botao-segmentos" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
              Buscar por segmento 
            </button>
            <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
              <li><a class="dropdown-item" href="#">Educação</a></li>
              <li><a class="dropdown-item" href="#">Lazer</a></li>
              <li><a class="dropdown-item" href="#">Serviços</a></li>
              <li><a class="dropdown-item" href="#">Saúde e Beleza</a></li>
            </ul>
          </div>         
    </Section>  
</template>

<script>
export default {

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
    width: 100%;
    background: #209532;
    border-radius: 4px;
    margin-bottom: 1rem;
}
</style>

