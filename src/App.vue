<script>
import axios from 'axios';
import { store } from './data/store';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
import AppMain from './components/AppMain.vue'
export default {
  name: 'pokedex',
  components: { AppMain },
  data: () => ({ store }),

};
</script>

<template>
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
