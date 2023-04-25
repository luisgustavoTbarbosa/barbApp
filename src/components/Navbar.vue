<template>
  <nav>
    <router-link to="/" class="logo-container">
      <img class="logo" src="@/assets/logo.svg" alt="Logo">
    </router-link>
    <div class="routes">
      <router-link to="/login" class="loginLink">Login</router-link>
      <router-link to="/signup" class="singUpLink">Cadastro</router-link>
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
    width: 100%;
    height: 4rem;
    padding: 0 2.2rem;
    background: #282830;
    color: #737380;

    &:has(.loginLink.router-link-active),
    &:has(.singUpLink.router-link-active) {
      position: fixed;
    }

    .logo-container {
      height: 1.5rem;

      .logo {
        height: 100%;
      }
    }
    
    .routes {
      display: flex;
      gap: 15px;
    
      a {
        color: #737380;
        text-decoration: none;
        font-size: 14px;

        &.router-link-active {
          color: #F6F6F6;
        }
      }
    }
  }
</style>