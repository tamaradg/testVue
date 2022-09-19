<template>
  <footer>
    <p>Copyright {{date}}</p>
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
