<template>
    <div :class="isPremium ? 'client-premium' : 'client'">
        <h4>Nome: {{ client.name }} </h4>
        <hr>
        <p>Email: {{ client.email }}</p>
        <p v-if="showAge === true">Idade: {{ client.age }}</p>
        <p v-else style="color: red; font-weight: bold;">Usuário teve sua idade escondida</p>
        <button @click="mudarCor($event)">Alternando entre usuário Premium & normal</button>
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
        },
        methods: {
            mudarCor: function($event) {
                console.log($event);
                this.isPremium = !this.isPremium;
            }
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