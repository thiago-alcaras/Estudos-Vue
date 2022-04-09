<template>
  <div class="app">
    <ButtonComponent></ButtonComponent>
    <ButtonRender></ButtonRender>
    <TitleComponent titulo="Titulo1"></TitleComponent>
  </div>
</template>

<script>
  import ButtonComponent from './components/ButtonComponent.vue';
  import ButtonRender from './components/ButtonRender.vue';
  import TitleComponent from './components/TitleComponent.vue';

export default {

  name: 'App',
  components: {
    ButtonComponent,
    ButtonRender,
    TitleComponent,
  }
}
</script>

<style>

</style>
