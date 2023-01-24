<script>
export default {
    name: 'AppMain',

}
</script>

<template>
    <main>
        <div class="main-container">
            <div class="row">
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

.col {
    flex-basis: 20%;
    height: 300px;
    padding: 1rem;
    border: 1px dashed yellow;

    .card {
        height: 100%;
        border: 1px solid black;
    }


}
</style>