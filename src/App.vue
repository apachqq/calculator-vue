<template>
    <div id="app">
        <div class="grid">
            <input type="text" v-model="result" placeholder="0">
            <button class="cell num" @click="input(number)" v-for="number in numbers">{{ number }}</button>
            <button class="cell op" @click="input(operation)" v-for="operation in operations">{{ operation }}</button>
            <button class="cell op" @click="reset">AC</button>
            <button class="cell op" @click="calculate">=</button>
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
        },
        methods: {
            input(char) {
                this.result += char
            },
            reset() {
                this.result = ''
            },
            calculate() {
                this.result = eval(this.result)
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
