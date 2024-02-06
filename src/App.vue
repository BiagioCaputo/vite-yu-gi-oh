<script>
import axios from 'axios';
import { store } from './data/store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
export default {
  name: 'Pokedex',
  components: { AppMain, AppHeader },
  data: () => ({ store }),

  methods: {
    fetchPokemons(endpoint) {
      store.isLoading = true;
      axios.get(endpoint).then(res => {
        const pokemons = res.data.docs.map(pokemon => {
          return {
            id: pokemon._id,
            name: pokemon.name,
            image: pokemon.imageUrl,
            number: pokemon.number,
            type1: pokemon.type1,
            type2: pokemon.type2

          }
        })

        store.pokemons = pokemons;
      }).catch(err => {
        console.error(err)
      }).then(() => {
        store.isLoading = false;
      })
    },

    searchPokemonsType(searchedType) {
      if (!searchedType) {
        this.fetchPokemons(endpoint)
      }
      else {
        const searchedTypeEndpoint = `${endpoint}/?eq[type1]=${searchedType}`;
        this.fetchPokemons(searchedTypeEndpoint)
      }
    }
  },

  created() {
    this.fetchPokemons(endpoint);
  }

};
</script>

<template>
  <AppHeader @change-type="searchPokemonsType" />
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
