<template>
    <div class="">
        <h1> {{titulo}} </h1>
        <h1> {{subtitulo}} </h1>
        <h1> {{tipo}} </h1>
    </div>
</template>

<script>
export default {
    name: 'TitleComponent',
    props: {
        titulo: {
            type: String,
            required: true,
            default: 'Titulo'
        },
        subtitulo: {
            type: String,
            required: false,
            default: 'Subtitulo'
        },
        tipo: {
            type: Number,
            validator(value) {
                return [1, 2, 3].includes(value);
            }
        }
    }
}
</script>

<style>

</style>