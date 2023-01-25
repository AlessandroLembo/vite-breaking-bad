<script>
export default {
    name: 'FilteredPokemon',

}
</script>

<template>
    <div class="filter-pokemon">
        <select name="pokemon" id="pokemon-type">
            <option value="fire">Fire</option>
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