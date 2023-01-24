<script>
import CardPokemon from './CardPokemon.vue';
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
                <!-- <div class="col">
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
                </div> -->
            </div>
        </div>
    </main>

</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables';

.main-container {
    border-radius: 10px;
    background-color: aliceblue;
    border: 1px solid black;
    padding: 2rem;
    margin-top: 3rem;

    .row {
        background-color: darkgray;
        display: flex;
        flex-wrap: wrap;
    }
}
</style>