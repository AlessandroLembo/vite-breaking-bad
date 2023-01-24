<script>
export default {
    name: 'AppHeader',

}
</script>

<template>
    <header>
        <div class="header-container">
            <h1 class="title">POKEMON</h1>
            <figure>
                <img src="../assets/img/poke.jpg" alt="logo">
            </figure>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables';

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
    }
}
</style>