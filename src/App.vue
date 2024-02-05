<script>
import { store } from './data/store';
import axios from 'axios';
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
