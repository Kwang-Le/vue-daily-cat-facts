<template>
  <div class="background">
    <CatFact />
  </div>
</template>

<script>
import CatFact from './components/CatFact.vue';
export default {
  name: 'App',
  components: {
    CatFact
  }
}
</script>

<style>
#app {
  font-family: 'Roboto', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.background {
  background-image: url("./assets/cat_image.jpg");
  height: 100vh;
  background-position:center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
