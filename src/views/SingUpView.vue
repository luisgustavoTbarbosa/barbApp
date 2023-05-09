<template>
  <main>
    <img class="logo" src="@/assets/logo.svg" alt="Logo">
    <h1>Cadastro</h1>
    <form class="singUp-container"  action="/login" method="post">
      <section v-show="this.count === 0">
        <label for="inputName">Nome</label>
        <input id="inputName" type="text" placeholder="João Pedro">

        <label for="inputSecondName">Sobrenome</label>
        <input id="inputSecondName" type="text" placeholder="Tranquilino Barbosa">

        <label for="inputMail">E-mail</label>
        <input id="inputMail" type="email" placeholder="tranquilino@gmail.com">
      </section>
      
      <section v-show="this.count === 1">
        <label for="inputBusinessName">Nome do seu negócio</label>
        <input id="inputBusinessName" type="text" placeholder="João estética e barba masculina">

        <label for="inputPhone">Telefone</label>
        <input id="inputPhone" type="tel" placeholder="(11) 999999999">

        <label for="inputPhoto">Foto de perfil</label>
        <input id="inputPhoto" type="url" placeholder="URL da foto"> 
      </section>

      <section v-show="this.count === 2" class="containerDays">
        <p>Quais dias da semana você trabalha?</p>

        <div>
          <div class="nameDays">Segunda-feira</div>
          <div class="nameDays">Terça-feira</div>
          <div class="nameDays">Quarta-feira</div>
          <div class="nameDays">Quinta-feira</div>
          <div class="nameDays">Sexta-feira</div>
          <div class="nameDays">Sábado</div>
          <div class="nameDays">Domingo</div>
        </div>
      </section>

      <div class="controls">
        <button  
          v-show="this.count > 0"
          class="backButton"
          type="button"
          @click="returningRegistrationSteps"
        >
          Voltar
        </button>
        <button
          v-show="this.count < 3"
          type="button"
          class="nextButton"
          @click="countingStepsRegistration"
        >
          Próximo
        </button>
    </div>
    </form>
  </main>
</template>

<script>
  export default {
    name: 'SingUpView',
    data() {
      return {
        count: 2
      }
    },
    methods: {
      countingStepsRegistration() {
        return this.count++
      },
      returningRegistrationSteps() {
        if(this.count === 0) {
          return
        }

        return this.count--
      }
    }
  }
</script>

<style lang="scss" scoped>
 main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0 2.2rem; 
    height: 100vh;
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

    .singUp-container {
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

        &::placeholder {
          color: #1e1e22;
        }
      }

      label + input {
        margin-bottom: 1.8rem;
      }

      .containerDays {
        p {
          color: #F6F6F6;
          font-size: 1rem;
        }

        > div {
          display: flex;
          flex-wrap: wrap;
          justify-content: center;
          gap: 0.5rem;
          margin-top: 1rem;
        }
      }

      .nameDays {
        background: #737380;
        padding: 0.5rem;
        border-radius: 6px;
      }

      .controls {
        display: flex;
        justify-content: space-between;
        gap: 20px;
        margin-top: 1.8rem;
      
        button {
          height: 2.9rem;
          background: #7028E4;
          border: none;
          border-radius: 4px;
          color: #F6F6F6;
          font-size: 1.1rem;

          &.nextButton {
            width: 100%;
          }

          &.backButton {
            width: 40%;
          }
        }
      }
    }
  }
</style>