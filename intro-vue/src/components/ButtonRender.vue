<template>
    <div class="">
        <button @click="increment()">
            Clicou {{ count }} vezes
        </button>
    </div>
</template>

<script>
export default {
    name: 'ButtonComponent',
    data() {
        return {
            count: 0,
        }
    },
    methods: {
        increment() {
            this.count++;
        }
    },
    render(createElement) {
        return createElement('button', {
            on: {
                click: this.increment
            }
        }, `Clicou ${this.count} vezes`);
    },
}
</script>

<style>

</style>