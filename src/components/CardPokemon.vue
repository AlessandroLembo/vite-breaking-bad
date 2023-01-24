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
            <div> {{ image.number }} </div>
            <h2> {{ image.name }} </h2>
            <h4><i> {{ image.type1 }} </i></h4>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables';

.col {
    flex-basis: 20%;
    height: 350px;
    padding: 1rem;
    border-radius: 10px;
}

.card {
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: whitesmoke;
    border-radius: 10px;

    img {
        height: 150px;
        width: 150px;
        border-radius: 50%;
    }
}

.card * {
    padding-bottom: 0.7rem;
}
</style>