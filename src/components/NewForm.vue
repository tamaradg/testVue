<template>
  <div>
    <form @submit.prevent="checkForm" v-if="!formSubmitted" >




      <span>Prénom</span><br>
      <input
        v-model="prenom"
        type="text"
        placeholder="Prénom"
      />
      <p>{{this.errorPrenom}}</p>

      <span>Nom</span><br>
      <input
        v-model="nom"
        type="text"
        placeholder="Nom"
      />

      <p>{{this.errorNom}}</p>


      <input
        class="submit"
        type="submit"
        value="Submit"
      >
    </form>
    <div v-if="formSubmitted">
      <h3>Bonjour {{prenom}} {{nom}}</h3>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        prenom: "",
        nom: "",
        formSubmitted: false,
        errorPrenom:"",
        errorNom:""

      };
    },
    methods: {
      // submitForm () {
      //   this.formSubmitted = true
      // },
      checkForm(e) {
        if (this.prenom && this.nom) {
          this.formSubmitted = true
        }

        this.errorPrenom = this.prenom.length > 3 ? "" : "Prénom trop court";

        this.errorNom = this.nom.length > 3 ? "" : "Nom trop court";


        e.preventDefault();
      }

    }
  }
</script>
<style scoped>
  form {
    padding: 10px;
    border: 2px solid black;
    border-radius: 5px;
  }

  input {
    padding: 4px 8px;
    margin: 4px;
  }

  span {
    font-size: 18px;
    margin: 4px;
    font-weight: 500;
  }

  .submit {
    font-size: 15px;
    color: #fff;
    background: #222;
    padding: 6px 12px;
    border: none;
    margin-top: 8px;
    cursor: pointer;
    border-radius: 5px;
  }
  p {
    color: red;
    font-weight: 300;
  }

  .error {
    border-color: red;
  }

</style>
