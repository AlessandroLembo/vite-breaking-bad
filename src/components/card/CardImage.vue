<script>
export default {
    name: 'CardImage',
    props: {
        image: String,
        number: Number,
        name: String,
        type: String
    },

}
</script>

<template>
    <div class="col">
        <div class="card">
            <img :src="image" :alt="name">
            <div> {{ number }} </div>
            <h2> {{ name }} </h2>
            <h4> {{ type }} </h4>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../../assets/scss/partials/variables' as *;

.col {
    flex-basis: 20%;
    height: 350px;
    padding: 1rem;
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

    // &.bkg-green {
    //     background-color: $green ;
    // }

    // &.bkg-blue {
    //     background-color: $lightblue ;
    // }

    // &.bkg-dodger {
    //     background-color: $dodger;
    // }

    // &.bkg-gold {
    //     background-color: $gold;
    // }
}

.card * {
    padding-bottom: 0.7rem;
}
</style>

