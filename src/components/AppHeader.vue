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
        <select name="type" @change="$emit('change-type', searchedType)" v-model="searchedType">
            <option value=''>All</option>
            <option v-for="(type, index) in this.types" :value="type">{{ type }}</option>
        </select>
    </header>
</template>

<style lang="scss" scoped></style>