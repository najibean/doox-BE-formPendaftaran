<template>
    <div id="app">
        <Daftar />
    </div>
</template>

<script>
import Daftar from "./components/formDaftar"

export default {
    name: "App",
    components: {
        Daftar,
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
