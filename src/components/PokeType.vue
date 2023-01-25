<script>
export default {
    name:'PokeType',
    data () {
        return {
            genres : [
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
            ],
            type: ''
        }
    },
    emits: ['change-type'],
    
}
</script>


<template>
    <select v-model="type" @change="$emit('change-type', type)" class="form-select w-25" aria-label="Default select example">
        <option selected>All</option>
        <option v-for="genre in genres"> {{genre}} </option>
        
    </select>

</template>

<style lang="scss" scoped>
    select {
            margin: 0 auto;
            text-align: center;
    }
</style>