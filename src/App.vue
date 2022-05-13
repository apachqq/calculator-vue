<template>
    <div id="app">
        <div class="grid">
            <input type="text" readonly v-model="result" placeholder="0">
            <button class="cell num" @click="input(number)" v-for="number in numbers">{{ number }}</button>
            <button class="cell op" @click="input(operation)" v-for="operation in operations">{{ operation }}</button>
            <button class="cell op" @click="reset">AC</button>
            <button class="cell op" @click="calculate">=</button>
        </div>
    </div>
</template>

<script>
    import AppMixin from '@/mixins/AppMixin'

    export default {
        mixins: [AppMixin]
    }
</script>

<style>
</style>
