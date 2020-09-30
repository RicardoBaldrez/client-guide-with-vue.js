<template>
    <div id='client'>
        <h2>{{ subtext }}</h2>
        <h3>Description of client ... </h3>
    </div>
</template>

<script>
    export default {
        name: 'Client',
        props: {
            subtext: String
        }
    }
</script>

<style scoped>
    #client {
        color: rgb(0, 255, 64);
        background-color: black;
        max-width: 600px;
        padding: 20px;
    }

    h2 {
        margin: 0 0 15px 0;
    }

    h3 {
        margin: 0;
    }
</style>