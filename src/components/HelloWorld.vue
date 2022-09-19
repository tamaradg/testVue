<template>
  <div class="hello">
    <h1>{{nom}}</h1>
    <h2>{{prenom}}</h2>
    <p v-if="afficheVille">{{ville}}</p>
    <p v-show="afficheDate">{{date}}</p>
    <ul>
      <!-- on boucle dans l'array en déclarant une key -->
      <li v-for="day in tableau" :key = "day">{{day}}</li>
    </ul>
    <!-- ici on affiche ou pas la date plus haut -->
    <button @click="afficheDate=!afficheDate">Afficher/masquer date</button>
    <button @click="count++">Vous avez clické {{count}} fois</button>
  </div>
</template>

<script>
// import { METHODS } from 'http';

export default {
  name: 'HelloWorld',
  // on stock les données à afficher ici
  data() {
    return {
      nom : "de Gaetano",
      prenom : "Tamara",
      ville : "Paris",
      date : new Date().toLocaleDateString(),
      afficheDate: true,
      afficheVille: true,
      tableau: ['lundi', 'mardi', 'mercredi', 'jeudi', 'vendredi', 'samedi', 'dimanche'],
      count: 0
    }
  },
  // on place les methodes apres la data
  methods : {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
