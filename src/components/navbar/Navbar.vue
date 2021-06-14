<template>
  <header class="container center">
    <nav class="navbar">
      <span class="botaonavbar">
        <span class="barra_botanavbar"></span>
        <span class="barra_botanavbar"></span>
        <span class="barra_botanavbar"></span>
      </span>
      <img
      src="src\assets\img\logo-clube-bem-bom.png"
      class="logobembom"
      alt="Logo Clube Bem Bom"
    />
    <img src="../../assets/img/face.svg" alt="avatar">    
    </nav>    
  </header>
</template>

<script>
export default {};
</script>

<style>
.container{
    width: 94%;
    margin: auto;
    margin-top: 10px;
}

.navbar {
    position: relative;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    padding-top: .5rem;
    padding-bottom: .5rem;
}

.logobembom {
  width: 81px;
}

.botaonavbar {
  width: 45px;
  height: 45px;
  border-radius: 5px;
  background-color: #005caa;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.barra_botanavbar {
  width: 28.71px;
  height: 3.03px;
  background: #ffffff;
  border-radius: 5px;
  margin: 2px;
}
.center{
    text-align: center;
}
</style>