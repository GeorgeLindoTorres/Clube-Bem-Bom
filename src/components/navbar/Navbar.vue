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
    <svg
      width="41"
      height="40"
      viewBox="0 0 41 40"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M13.75 32.5625C16.125 33.8125 18.375 34.4375 20.5 34.4375C22.625 34.4375 24.8438 33.8125 27.1562 32.5625C29.5312 31.3125 31.3125 29.7812 32.5 27.9688C32.4375 26.2188 31.0312 24.75 28.2812 23.5625C25.5312 22.375 22.9375 21.7812 20.5 21.7812C18.0625 21.7812 15.4688 22.375 12.7188 23.5625C9.96875 24.6875 8.5625 26.1562 8.5 27.9688C9.6875 29.7812 11.4375 31.3125 13.75 32.5625ZM24.7188 7.8125C23.5312 6.625 22.125 6.03125 20.5 6.03125C18.875 6.03125 17.4688 6.625 16.2812 7.8125C15.0938 9 14.5 10.4063 14.5 12.0312C14.5 13.6562 15.0938 15.0625 16.2812 16.25C17.4688 17.4375 18.875 18.0312 20.5 18.0312C22.125 18.0312 23.5312 17.4375 24.7188 16.25C25.9062 15.0625 26.5 13.6562 26.5 12.0312C26.5 10.4063 25.9062 9 24.7188 7.8125ZM6.34375 5.9375C10.2812 2 15 0.03125 20.5 0.03125C26 0.03125 30.6875 2 34.5625 5.9375C38.5 9.8125 40.4688 14.5 40.4688 20C40.4688 25.5 38.5 30.2188 34.5625 34.1562C30.6875 38.0312 26 39.9688 20.5 39.9688C15 39.9688 10.2812 38.0312 6.34375 34.1562C2.46875 30.2188 0.53125 25.5 0.53125 20C0.53125 14.5 2.46875 9.8125 6.34375 5.9375Z"
        fill="#3B9F4B"
      />
    </svg>
    </nav>    
  </header>
</template>

<script>
export default {};
</script>

<style>
.container{
    width: 100%;
    padding-right: var(--bs-gutter-x,1rem);
    padding-left: var(--bs-gutter-x,1rem);
    margin-right: auto;
    margin-left: auto;
    margin-top: 1rem;
    margin-top: 1rem;
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