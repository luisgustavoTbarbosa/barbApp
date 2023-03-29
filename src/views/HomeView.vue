<template>
  <main>
    <div class="banner-container">
      <img src="@/assets/banner_home.png" alt="Imagem de uma barbearia">
    </div>
    <div class="content">
      <h1>O melhor app para o seu negócio</h1>
      <p>Gerencie os seus horários, clientes e ganhos.</p>
      <router-link to="/login" class="button-init-boost">Iniciar boost</router-link>
    </div>
  </main>
</template>

<script>
  export default {
    name: 'HomeView'
  }
</script>

<style lang="scss" scoped>
  main {
    height: calc(100vh - 4rem);
    background: #19191C;
  }

  .banner-container {
    height: 10rem;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  .content {
    padding: 2.5rem 2.2rem 0;
    color: #F6F6F6;

    h1 {
      margin-bottom: 1.5rem;
      font-size: 2.3rem;
      font-weight: 500;
    }

    p {
      margin-bottom: 1.5rem;
      font-size: 1rem;
    }

    .button-init-boost {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 13rem;
      height: 2.5rem;
      background: linear-gradient(180deg, #C086D2 0%, #A769D8 14.58%, #7028E4 68.23%);
      border: none;
      border-radius: 5px;
      color: #F6F6F6;
      font-size: 1rem;
      text-decoration: none;
      cursor: pointer;
    }
  }
</style>