<script>
import axios from 'axios';
import PokeList from './PokeList.vue';
export default {
    components: {PokeList},
    data(){
    return {
      pokemons: []
    }
  },
  created (){
    axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=10&page=1')
    .then(response => {
        this.pokemons = response.data.docs;
    })
  }
}
</script>

<template>
    <main>
        <poke-list v-for="pokemon in pokemons"
    
         :image="pokemon.imageUrl"
         :number="pokemon.number"
         :name="pokemon.name" 
         :type1="pokemon.type1" 
         @key="pokemon.id">
    
        </poke-list>
    </main>
</template>

<style lang="scss" scoped>

</style>