<template>
    <game />
</template>

<script>
import Game from './components/game'
export default {
    components: {
        Game
    }
}
</script>

<style>
html {
    height: 100%;
}
body {
    margin: 0;
    height: 100%;
}
#app {
    height: 100%;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background: #40474a;
}
</style>
