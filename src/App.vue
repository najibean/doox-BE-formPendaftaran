<template>
    <div id="app">
        <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
        <FormPendaftaran />
    </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import FormPendaftaran from "./components/formPendaftaran"

export default {
    name: "App",
    components: {
        // HelloWorld,
        FormPendaftaran,
    },
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
