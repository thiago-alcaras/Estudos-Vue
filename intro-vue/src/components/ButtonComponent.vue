<template>
    <div class="">
        <button @click="increment()">
            Clicou {{ count }} vezes
        </button>
        <button @click="incrementProp()">
            Clicou {{ $data.$count1 }} vezes no botão prop
        </button>
    </div>
</template>

<script>
export default {
    name: 'ButtonComponent',
    data() {
        return {
            count: 0,
            $count1: 0,
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