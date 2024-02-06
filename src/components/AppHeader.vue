<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            types: [
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water"
            ],

            searchedType: '',
        }
    },
    emits: ['change-type']

};
</script>

<template>
    <header class="p-3 text-end">
        <div class="container d-flex justify-content-between">
            <h1>Pokedex</h1>
            <select name="type" class="select-type" @change="$emit('change-type', searchedType)" v-model="searchedType">
                <option value=''>All</option>
                <option v-for="type in this.types" :value="type">{{ type }}</option>
            </select>
        </div>
        
    </header>
</template>

<style lang= "scss" scoped>
h1{
    font-weight: bold;
    font-size: 50px;
}
</style>