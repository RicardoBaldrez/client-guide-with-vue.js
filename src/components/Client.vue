<template>
    <div :class="{'client' : !isPremium, 'client-premium' : isPremium}">
        <h4>Nome: {{ client.name }} </h4>
        <hr>
        <p>Email: {{ client.email }}</p>
        <p v-if="showAge === true">Idade: {{ client.age }}</p>
        <p v-else style="color: red; font-weight: bold;">Usuário teve sua idade escondida</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isPremium: true
            }
        },
        props: {
            client: Object,
            showAge: Boolean
        }
    }
</script>

<style scoped>
    .client {
        max-width: 600px;
        background-color: #f0f0f0;
        padding: 2%;
        margin-bottom: 10px;
        border-radius: 5px;
    }

    .client-premium {
        max-width: 600px;
        background-color: #ffc400;
        padding: 2%;
        margin-bottom: 10px;
        border-radius: 5px;
    }

    h4, p:last-child {
        margin: 0;
    }
</style>