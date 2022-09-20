<template>
  <div>
    <ul>
      <li ref="months" v-for="d in date" :key = "d">{{d}}</li>
    </ul>
  </div>
</template>

<script>
 export default {
  name: "MonthsCompo",
  data() {
    return {
      date: ['janvier','fevrier','mars','avril','mai','juin','juillet','aout','septembre','octobre','novembre','decembre']
    }
  },
mounted(){
console.log(this.$refs.months);
console.log(this.$refs);
}
 }
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
</style>
