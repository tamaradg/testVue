<template>

   <!-- on utilise les nouveau composants ici -->
  <HeaderCompo/>
  <HelloWorld/>
  <NewComposant/>
  <FooterCompo/>
</template>

<script>
  // on importe les nouveaux composants ici
import HelloWorld from './components/HelloWorld.vue'
import NewComposant from './components/new-composant.vue'
import HeaderCompo from "./components/HeaderCompo.vue";
import FooterCompo from "./components/FooterCompo.vue";

export default {
  name: 'App',
  // pour utiliser un component on le déclare ici
  components: {
    HelloWorld,
    NewComposant,
    HeaderCompo,
    FooterCompo
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
