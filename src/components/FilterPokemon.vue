<script>
import axios from 'axios';


export default {
    name: 'FilteredPokemon',
    data() {
        return {
            types: [],
            chooseValue: '',
        }
    },

    methods: {
        fetchTypes() {
            axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons/types1')
                .then((res) => {
                    this.types = res.data;
                })
        },
    },

    created() {
        this.fetchTypes()
    },

    emits: ['value-change']

}
</script>

<template>
    <div class="filter-pokemon">
        <select name="pokemon" id="pokemon-type" @change="$emit('value-change', chooseValue)" v-model="chooseValue">
            <option value="" selected disabled hidden>Select type</option>
            <option selected="selected" value="All">All</option>
            <option v-for="type in types" :key="type" :value=type>
                {{ type }} </option>
        </select>
    </div>
</template>

<style scoped lang="scss">
.filter-pokemon {
    display: flex;
    margin: 1rem;
}

#pokemon-type {
    width: 200px;
    padding: 10px;
    border-radius: 5px;
    background-color: aliceblue;
    font-size: 20px;
}
</style>