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
    fetchPokemons() {
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
    }
  },

  created() {
    this.fetchPokemons();
  }

};
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
