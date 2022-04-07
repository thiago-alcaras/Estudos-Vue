<template>
  <div class="app">
    <ButtonComponent></ButtonComponent>
    <ButtonRender></ButtonRender>
  </div>
</template>

<script>
  import ButtonComponent from './components/ButtonComponent.vue';
  import ButtonRender from './components/ButtonRender.vue';

export default {

  name: 'App',
  components: {
    ButtonComponent,
    ButtonRender,
  }
}
</script>

<style>

</style>
