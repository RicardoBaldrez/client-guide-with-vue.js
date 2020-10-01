<template>
  <div id="app">
    <h1>Guide of clients</h1>
    <Client :client="clientDefault" :showAge="false" />
    <Client :client="clientDefault" :showAge="true" />
    <Client :client="clientDefault" :showAge="false" />
  </div>
</template>

<script>
  import Client from './components/Client';

  export default {
    name: 'App',
    data() {
      return {
        nameDefault: 'Ricardo Barbosa',
        clientDefault: {
          name: "Nathália",
          email: "nathaliaop.2@hotmail.com",
          age: "26"
        }
      }
    },
    components: {
      Client
    }
  }
</script>

<style>

</style>