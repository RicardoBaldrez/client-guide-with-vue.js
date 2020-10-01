<template>
    <div id='client'>
        <h4>Nome: {{ client.name }} </h4>
        <p>Email: {{ client.email }}</p>
        <p>Idade: {{ client.age }}</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                
            }
        },
        props: {
            name: String,
            email: String,
            age: Number,
            client: Object
        }
    }
</script>

<style scoped>
    #client {
        max-width: 600px;
        background-color: #ece5e3;
        padding: 2%;
        margin-bottom: 10px;
    }

    h4, p:last-child {
        margin: 0;
    }
</style>