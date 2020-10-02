<template>
  <div id="app">
    <h1>Guide of clients</h1>
    
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
        clients: [
          {
            id: 1,
            name: "Nathália",
            email: "nathaliaop.2@hotmail.com",
            age: "26",
            showAge: true
          },
          {
            id: 2,
            name: "Ricardo",
            email: "ricardo.baldrez@gmail.com",
            age: "30",
            showAge: false
          },
          {
            id: 3,
            name: "Maria",
            email: "maria.baldrez@gmail.com",
            age: "59",
            showAge: true
          },
        ]
      }
    },
    components: {
      Client
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
</style>