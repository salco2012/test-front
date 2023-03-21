<template>
  <div id="app">
    <main-component />
  </div>
</template>

<script>
import MainComponent from './components/MainComponent.vue';

export default {
  name: 'App',
  components: {
    MainComponent,
  }
}
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.3rem;
  margin: 10px;
}
</style>
