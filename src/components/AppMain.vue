<script>
import CardPokemon from './CardPokemon.vue';
import { store } from '../data/store';
export default {
    name: 'AppMain',
    components: { CardPokemon },
    data: () => ({ store })

};
</script>

<template>
    <main class="d-flex align-items-center justify-content-center">
        <AppLoader v-if="store.isLoading" label="Pokemons" />
        <div v-else class="row-container py-3">
            <div class="row row-cols-2 row-cols-md-3 row-cols-xl-5 row-cols-xxl-6  gap-4 justify-content-center">
                <div class="col" v-for="pokemon in store.pokemons" :key="pokemon.id">
                    <CardPokemon :name="pokemon.name" :image="pokemon.image" :numberPokedex="pokemon.number"
                        :type1="pokemon.type1" :type2="pokemon.type2" />
                </div>
            </div>


        </div>

    </main>
</template>

<style lang="scss" scoped>
main {
    height: 100%;

    .row-container {
        width: 80%;
        background-image: url('https://wallpapercave.com/wp/wp3170189.jpg');
        background-size: 50%;
        background-repeat: repeat;
        border: 1px solid lightgreen;
        overflow-y: auto;
        overflow-x: hidden;
    }
}
</style>
