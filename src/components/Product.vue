<template>
  <div>
      <h3>My product</h3>
      <p>{{ description }}</p>
      <input type="text" placeholder="$ ...">
  </div>
</template>

<script>
    export default {
        name: 'Product',
        props: {
            description: String
        }
    }
</script>

<style>

</style>