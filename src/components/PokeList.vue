<script>
export default {
  name: 'Pokedex',
  props: {
    image: String,
    number: Number,
    name: String,
    type1: String,
  }
}
</script>

<template>
    <section id="pokemons" class="container">
        <div class="row row-cols-3 g-3">
            <div class="col">
                <img :src="image" alt="">
                <div> {{ number }} </div>
                <h2> {{ name }} </h2>
                <div>  {{ type1 }} </div>
            </div>
        </div>
  </section>
</template>

<style scoped>

</style>