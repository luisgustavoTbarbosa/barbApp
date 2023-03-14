<template>
  <nav>
    <router-link to="/">
      <img class="logo" src="@/assets/logo.svg" alt="Logo">
    </router-link>
    <div class="routes">
      <router-link to="/login">Login</router-link>
      <router-link to="/signup">Cadastro</router-link>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'Navbar'
  }
</script>

<style lang="scss" scoped>
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 60px;
    padding: 0 20px;
    background: #282830;
    color: #737380;
    
    a {
      color: #737380;
      text-decoration: none;
    }

    .logo {
      height: 20px;
    }

    .routes {
      display: flex;
      gap: 15px;
    }
  }
</style>