<script>
// All files imported
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
      store,

      // general Api pokemon call
      apiUri: 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons',
    }
  },


  methods: {

    // method to call Api Pokemon
    fetchImages(url) {
      axios.get(url)
        .then((res) => {
          store.images = res.data.docs;
        });
    },

    // method to filter Api call by pokemon type
    selectPokemonType(item) {
      if (item === 'All') {
        const allType = ('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=20&page=8')
        this.fetchImages(allType);

      } else {
        const url = `${this.apiUri}?q[type1]=${item}`
        this.fetchImages(url);
      }
    }
  },

  created() {
    this.fetchImages('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=20&page=8')
  }
}
</script>

<template>
  <div class="container">
    <div class="wrapper">

      <!-- use header component -->
      <app-header></app-header>
      <div class="main-container">

        <!-- use custom event in filter-component to receive data -->
        <filter-pokemon @value-change="selectPokemonType"></filter-pokemon>
        <div class="row">

          <!-- use component app cols to print pokemon cards -->
          <app-cols v-for="image in store.images" :key="image.id" :image="image.imageUrl" :number="image.number"
            :name="image.name" :type="image.type1"></app-cols>
        </div>
      </div>
    </div>

  </div>
</template>

<style lang="scss">
// Style of App.vue imported by file style.scss
@use './assets/scss/style.scss';
</style>