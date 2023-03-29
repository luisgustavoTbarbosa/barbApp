<template>
  <main>
    <img class="logo" src="@/assets/logo.svg" alt="Logo">

    <h1>Login</h1>

    <div class="login-container">
      <label for="inputMail">Seu e-mail</label>
      <input id="inputMail" type="email" placeholder="joseph@gmail.com">
      <label for="inputPassword" class="labelPassword">Sua senha</label>
      <input id="inputPassword" type="password" placeholder="JskdX2#">
      <button>Entrar</button>
    </div>

    <p>Ainda não possui uma conta? <router-link to="/signup" class="signup">Cadastre-se</router-link></p>
  </main>
</template>

<script>
  export default {
    name: 'LoginView'
  }
</script>

<style lang="scss" scoped>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0 2.2rem;
    height: calc(100vh - 4rem);
    background: #19191C;

    .logo {
      width: 100px;
    }

    h1 {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      width: 100%;
      margin-top: 1.1rem;
      color: #F6F6F6;
      font-weight: 500;
      font-size: 1.2rem;

      &::after {
        content: '';
        height: 2px;
        width: 100%;
        background: #737380;
      }
    }

    .login-container {
      width: 100%;
      margin-top: 1.1rem;
      padding: 1.5rem;
      background: #212124;
      border-radius: 8px;

      label {
        color: #F6F6F6;
        font-size: 1rem;

        &.labelPassword {
          display: flex;
          align-items: flex-end;
          justify-content: space-between;

          &::after {
            content: 'Esqueceu a senha?';
            color: #0085FF;
            font-size: .9rem;
            cursor: pointer;
          }
        }
      }

      input {
        display: block;
        width: 100%;
        height: 2.2rem;
        margin-top: .72rem;
        padding: 0 .72rem;
        border: none;
        border-radius: 4px;
        background: #737380;
        color: #1e1e22;
        font-size: 1rem;

        &#inputMail {
          margin-bottom: 1.8rem;
        }

        &::placeholder {
          color: #1e1e22;
        }
      }

      button {
        width: 100%;
        height: 2.9rem;
        margin-top: 1.8rem;
        background: #7028E4;
        border: none;
        border-radius: 4px;
        color: #F6F6F6;
        font-size: 1.1rem;
      }
    }

    p {
      align-self: flex-start;
      margin-top: 1.1rem;
      color: #F6F6F6;
      font-size: .9rem;

      .signup {
        margin-left: .4rem;
        color: #0085FF;
        text-decoration: none;
      }
    }
  }
</style>