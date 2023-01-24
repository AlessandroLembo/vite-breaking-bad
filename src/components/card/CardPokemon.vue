<script>
import axios from 'axios';
import CardImage from './CardImage.vue';
import { store } from '../../data/store';

export default {
    name: 'CardPokemon',
    components: { CardImage },
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
    <card-image v-for="image in store.images" :key="image.id" :image="image.imageUrl" :number="image.number"
        :name="image.name" :type="image.type1"></card-image>
</template>

<style>

</style>