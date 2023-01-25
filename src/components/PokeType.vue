<script>
export default {
    name:'PokeType',
    data () {
        return {
            types : [
                        "Steel",
                        "Fire",
                        "Fairy",
                        "Normal",
                        "Dragon",
                        "Dark",
                        "Electric",
                        "Poison",
                        "Fighting",
                        "Rock",
                        "Ghost",
                        "Psychic",
                        "Grass",
                        "Bug",
                        "Ice",
                        "Flying",
                        "Water",
                        "Ground"
            ]
        }
    }
}
</script>


<template>
    <select class="form-select w-25" aria-label="Default select example">
        <option  selected>All</option>
        <option v-for="type in types"> {{type}} </option>
        
    </select>

</template>



<style lang="scss" scoped>
    select {
            margin: 0 auto;
            text-align: center;
    }
</style>