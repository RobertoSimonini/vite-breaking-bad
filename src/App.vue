<script>
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue'
import {store} from './store.js'
import axios from 'axios';
export default {
  name: 'App',
  components: {AppMain, AppHeader},
  data () {
    return {
      store
    }
  },

  methods: {
    fetchPokemon (url){
      axios.get(url)
    .then(response => {
        store.pokemons = response.data.docs;
    })
  }
},

created (){
this.fetchPokemon(store.apiUrl)
}
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