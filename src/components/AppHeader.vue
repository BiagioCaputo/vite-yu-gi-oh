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
            ]
        }
    }

};
</script>

<template>
    <header>
        <select name="type">
            <option value="all">All</option>
            <option v-for="(type, index) in this.types" :value="type">{{ type }}</option>
        </select>

    </header>
</template>

<style lang="scss" scoped></style>