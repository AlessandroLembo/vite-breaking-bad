<script>
import axios from 'axios';
// import CardImage from './CardImage.vue';
export default {
    name: 'CardPokemon',
    // components: { CardImage },
    data() {
        return {
            images: []
        }
    },
    created() {
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=10&page=8')
            .then((res) => {
                this.images = res.data.docs;
            })
    }
}
</script>

<template>
    <div v-for="image in images" :key="image.id" class="col">
        <div class="card">
            <img :src="image.imageUrl">
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables';

.col {
    flex-basis: 20%;
    height: 350px;
    padding: 1rem;
    border: 1px dashed yellow;

}

.card {
    border: 1px solid black;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;

    img {
        height: 150px;
        width: 150px;
        border-radius: 50%;
    }
}
</style>