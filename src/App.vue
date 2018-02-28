<template>
  <div id="app">
    <!-- <first> </first> -->
    <Gestiondog> </Gestiondog>
    
  </div>
</template>

<script>
import First from './components/First.vue';
import Gestiondog from './components/Gestiondog.vue';


export default {
  name: 'app',
  components: {
    Gestiondog,
    First
  }
}
</script>

<style lang="scss">
 @import "./assets/custom.scss";
 @import "../node_modules/bootstrap/scss/bootstrap.scss";
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
