<script>
export default {
  name: 'Pokedex',
  props: {
    image: String,
    number: Number,
    name: String,
    type1: String,
  },
  
}
</script>

<template>
            <div class="col-4 card" role="button">
                <img :src="image" alt="">
                <div class="pt-3"> #{{ number }} </div>
                <h2> {{ name }} </h2>
                <div class="fw-bold">  {{ type1 }} </div>
            </div>
</template>

<style lang="scss" scoped>

    .card {
        background-color: transparent;
        border: none;
        transition: 0.25s;

        &:hover {
            transform: scale(1.05);
        }
    }

    img {
        height: 400px;
        background-color: transparent;
        box-shadow: 0 0 10px black;

    }
</style>