<template>
    <div id="app">
        <div class="grid">
            <input type="text" placeholder="0">
            <button class="cell num"></button>
            <button class="cell op"></button>
            <button class="cell op"></button>
            <button class="cell op"></button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                result: '',
                numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9, 0],
                operations: ['+', '-', '*', '/']
            }
        }
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
