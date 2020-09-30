<template>
  <div id="app">
    <h1>Guide of clients</h1>
    <Client subtext="Client here!" />
    <hr>
    <h4>List of products</h4>
    <Product description="Description of the product" />
  </div>
</template>

<script>
  import Client from './components/Client';
  import Product from './components/Product';

  export default {
    name: 'App',
    components: {
      Client,
      Product
    }
  }
</script>

<style>

</style>