<template>
  <div>Je suis un composant</div>
</template>

<script>
  export default {
    name: 'MonComposant'
  }
</script>
<!-- le scoped permet d'appliquer du css sur ce composant sans toucher les autres -->
<style scoped>
  div {
    color: maroon
  }
</style>
