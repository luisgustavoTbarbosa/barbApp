<template>
  <Navbar />
  <router-view/>
</template>

<script>
  import Navbar from '@/components/Navbar.vue'

  export default {
    components: {
      Navbar
    }
  }
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto';
  }

  html {
    @media (max-width: 1080px) {
        font-size: 93.75%; //15px
    }
    @media (max-width: 720px) {
        font-size: 87.5%; //14px
    }
  }
</style>
