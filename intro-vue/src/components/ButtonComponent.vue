<template>
    <div class="">
        <div class="buttons">
            <button @click="increment">
                Clicou {{ count }} vezes
            </button>
            <button @click="incrementProp()">
                Clicou {{ $data.$count1 }} vezes no botão prop
            </button>
        </div>

        <div class="nome">
            <span>Nome: {{nome}}</span>
            <input type="text" v-model="nome"/>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ButtonComponent',
    data() {
        return {
            count: 0,
            $count1: 0,
            nome: "Thiago"
        }
    },
    methods: {
        increment() {
            this.count++;
        },
        incrementProp() {
            this.$data.$count1++;
        }
    }
}
</script>

<style>

</style>