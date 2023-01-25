<script>
import axios from 'axios';
import { store } from './data/store';
import AppHeader from './components/AppHeader.vue';
import AppCols from './components/AppCols.vue';
import FilterPokemon from './components/FilterPokemon.vue';


export default {
  name: 'App',
  components: { AppHeader, AppCols, FilterPokemon },
  data() {
    return {
      store
    }
  },


  methods: {
    fetchImages(url) {
      axios.get(url)
        .then((res) => {
          store.images = res.data.docs;
        });
    }
  },

  created() {
    this.fetchImages('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=10&page=8')
  }
}
</script>

<template>
  <div class="container">
    <div class="wrapper">
      <app-header></app-header>
      <div class="main-container">
        <filter-pokemon @type-change=""></filter-pokemon>
        <div class="row">
          <app-cols v-for="image in store.images" :key="image.id" :image="image.imageUrl" :number="image.number"
            :name="image.name" :type="image.type1"></app-cols>
        </div>
      </div>
    </div>

  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>