<script>
export default {
    name: 'AppHeader',

}
</script>

<template>
    <header>
        <div class="header-container">
            <div class="left-header"></div>
            <div class="right-header"></div>


        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables';

.header-container {
    height: 150px;
    border: 1px dashed black;
    display: flex;
    flex-wrap: wrap;

    .left-header,
    .right-header {
        flex-basis: 50%;
        border: 1px solid yellow;
    }
}
</style>