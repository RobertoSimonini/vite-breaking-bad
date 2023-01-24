<script>
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue'
export default {
  name: 'App',
  components: {AppMain, AppHeader}

}
</script>

<template>
  <app-header></app-header>
  <app-main></app-main>
</template>

<style>
  body{
    min-height: 100vh;
    background-color: rgb(197,41,25);
  }
</style>