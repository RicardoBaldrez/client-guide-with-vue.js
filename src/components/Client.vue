<template>
    <div id='client'>
        <input type="text" name="name" id="name" v-model="name">
        <hr>
        <h2 id='name-client'>{{ name }}</h2>
        <p>Description of client: {{ description }} </p>
        <hr>
        <input type="text" name="age" id="age" :value="age">
    </div>
</template>

<script>
    export default {
        data() {
            return {
                name: 'Ricardo',
                email: 'ricardo.baldrez@gmail.com',
                age: 30,
                description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s.'
            }
        }
    }
</script>

<style scoped>
    #client {
        max-width: 600px;
    }

    h2 {
        margin: 0 0 15px 0;
    }

    h3 {
        margin: 0;
    }
</style>