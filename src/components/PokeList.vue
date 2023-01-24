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
            <div class="col-3 card">
                <img :src="image" alt="">
                <div> #{{ number }} </div>
                <h2> {{ name }} </h2>
                <div class="fw-bold">  {{ type1 }} </div>
            </div>
</template>

<style scoped>
    img {
        height: 300px;
    }
</style>