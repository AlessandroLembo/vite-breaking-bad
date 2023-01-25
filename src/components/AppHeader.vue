<script>
// import FilterPokemon from './FilterPokemon.vue';
export default {
    // components: { FilterPokemon },
    name: 'AppHeader',

}
</script>

<template>
    <header>
        <div class="header-container">
            <!-- <filter-pokemon></filter-pokemon> -->
            <h1 class="title">POKEMON</h1>
            <figure>
                <img src="../assets/img/poke.jpg" alt="logo">
            </figure>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables' as *;

.header-container {
    height: 150px;
    display: flex;
    justify-content: space-around;
    align-items: center;

    .title {
        font-weight: bold;
        font-size: 60px;
        color: yellow;
        text-shadow: 2px 2px dodgerblue;
    }

    img {
        height: 120px;
        border-radius: 10px;
        box-shadow: 0 0 6px 3px black;
    }
}
</style>