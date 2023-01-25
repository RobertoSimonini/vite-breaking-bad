<script>
import {store} from '../store'
import PokeList from './PokeList.vue';
export default {
    components: {PokeList},
    data () {
    return store
  }
  
}
</script>

<template>
    <main>
    <section id="pokemons" class="container text-center my-4">
        <div class="row g-4 justify-content-between">
        
        <poke-list v-for="pokemon in pokemons"
    
         :image="pokemon.imageUrl"
         :number="pokemon.number"
         :name="pokemon.name" 
         :type1="pokemon.type1" 
         @key="pokemon.id">
    
        </poke-list>
    </div>
  </section>
    
    </main>
</template>

<style lang="scss" scoped>
  #pokemons {
    background-color: rgb(90,93,102);
    padding: 2rem;
    border-radius: 10px;

  }

 

  
</style>