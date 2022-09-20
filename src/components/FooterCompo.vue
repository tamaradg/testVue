<template>
  <footer>
    <!-- le &copy correspond au petit logo du copyright -->
    <p>Copyright &copy; {{date}}</p>
    <a href="mention.html">Mentions légales</a>
  </footer>
</template>

<script>
  export default {
    name: 'FooterCompo',
    data() {
      return {
        date : new Date().getFullYear()
      }
    }
  }
</script>

<style scoped>

</style>
