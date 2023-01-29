<script>
import { colorMap } from '../data/index'
export default {
    name: 'Pokedex',
    props: {
        image: String,
        number: Number,
        name: String,
        type1: String,
    },
    computed: {
        bgColor() {
            return colorMap [this.type1]
        }
    }

}
</script>

<template>
    <div class="card d-flex align-items-center justify-content-center" :style="`background-color: ${bgColor}`">
        <img :src="image" alt="">
            <div class="pt-3"> #{{ number }} </div>
            <h4> {{ name }} </h4>
            <div class="fw-bold"> {{ type1 }} </div>
    </div>
</template>

<style lang="scss" scoped>
.card {
    flex-basis: 18%;
    padding: 0;
    height: 300px;
    

    box-shadow: 0 0 10px black;
    cursor: pointer;
}

img {
    height: 125px;
    width: 125px;
    border-radius: 50%;
    background-color: transparent;
    border: 1px solid black;
    object-position: center;
}
</style>