<script>
import axios from 'axios';
export default {
    name: 'CardPokemon',
    data() {
        return {
            images: []
        }
    },
    created() {
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=10&page=1')
            .then((res) => {
                this.images = res.data.docs;
            })
    }
}
</script>

<template>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

        </div>
    </div>
    <div class="col">
        <div class="card">

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

    .card {
        height: 100%;
        border: 1px solid black;
        border-radius: 10px;
    }


}
</style>