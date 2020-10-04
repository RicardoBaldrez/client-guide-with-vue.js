<template>
  <div id="app">
    <h1>Guide of clients</h1>

    <hr>

    <h3>Cadastro:</h3>
    <input type="text" placeholder="name" v-model="nameField">
    <input type="email" placeholder="email" v-model="emailField">
    <input type="number" placeholder="age" v-model="ageField">
    <button @click="registerUser">Cadastrar</button>
    <p class="error-form" v-if="gaveError">Verifique os campos e tente novamente!!!</p>
    <hr>

    <div v-for="(client, index) in clients" :key="client.id">
      <p>{{ index }}</p>
      <Client :client="client" :showAge="client.showAge" />
    </div>
  </div>
</template>

<script>
  import Client from './components/Client';

  export default {
    name: 'App',
    data() {
      return {
        nameField: '',
        emailField: '',
        ageField: '',
        gaveError: false,
        clients: [
          {
            id: 1,
            name: "Nathália",
            email: "nathaliaop.2@hotmail.com",
            age: "26",
            showAge: true
          }
        ]
      }
    },
    components: {
      Client
    },
    methods: {
      registerUser: function() {
        if (this.nameField == '' || this.emailField == '' || this.ageField == '') {
          this.gaveError = true;
        } else {
          this.gaveError = false;
          this.clients.push({ id: Date.now(), name: this.nameField, email: this.emailField, age: this.ageField });
          this.nameField = "";
          this.emailField = "";
          this.ageField = "";
        }
      }
    }
  }
</script>

<style>
  #app {
    max-width: 600px;
    margin: 0 auto;
  }

  h1 {
    text-align: center;
  }

  .error-form {
    color: red;
    font-weight: bold;
    font-size: 1.2em;
  }
</style>