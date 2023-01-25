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
            <div class="card d-flex align-items-center">
                <img :src="image" alt="">
                <div class="card-text">
                    <div class="pt-3"> #{{ number }} </div>
                    <h2> {{ name }} </h2>
                    <div class="fw-bold">  {{ type1 }} </div>
                </div>
            </div>
</template>

<style lang="scss" scoped>

    .card {
        flex-basis: 30%;
        padding: 0;
        cursor: pointer;
    
        box-shadow: 0 0 10px black;

        .card-text {
            background-color: #F6DFA4;
            width: 100%;

        }
    }

    img {
        height: 300px;
        width: 300px;
        transform: scale(0.5);
        border-radius: 50%;
        background-color: transparent;
        border: 1px solid black;
        object-position: center;       
    }

</style>