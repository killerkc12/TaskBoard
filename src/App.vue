<template>
  <div class="app">
    <header-component />
    <board-compoent />
  </div>
</template>

<script>

import HeaderComponent from './components/HeaderComponent.vue'
import BoardCompoent from './components/BoardComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    BoardCompoent
  },
};
</script>
<style>
body {
  margin: 0;
  padding: 0;
  font-family: Roboto;
  background: #F6F8F9;
}
</style>