<script>
import CardPokemon from './card/CardPokemon.vue';
export default {
    name: 'AppMain',
    components: { CardPokemon },

}
</script>

<template>
    <main>
        <div class="main-container">
            <div class="row">
                <card-pokemon></card-pokemon>

            </div>
        </div>
    </main>

</template>

<style lang="scss">
@use '../assets/scss/partials/variables' as *;

.main-container {
    border-radius: 10px;
    background-color: aliceblue;
    padding: 2rem;

    .row {
        background-color: darkgray;
        display: flex;
        flex-wrap: wrap;
        border-radius: 10px;
    }
}
</style>