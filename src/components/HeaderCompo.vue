<template>
  <div class="header">
    <img alt="Vue logo" src="../assets/logo.png">
    <div>
      <h1>{{prenom}}</h1>
      <h2>{{nom}}</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderCompo',
  data() {
    return {
      prenom: 'Tamara',
      nom: "DG"
    }
  }
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-around;
}

</style>
