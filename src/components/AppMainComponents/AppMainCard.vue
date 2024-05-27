<script>
import dataCard from "../../data/dataCard.js";
import store from "../../data/store.js";
export default {
    props: {

    },
    components: {

    },
    data() {
        return {
            // variabile utente per l'archetipo
            sceltaUtente: "Alien",
            // DATI DA UN MIO ARRAY
            dataCard,
            // DATI DA AXIOS
            store,
        }
    },
}
</script>

<template>
    <section class="container bg-white p-3">
        <!-- se la scelta dell'utente è archetype alien allora moistro gli archetype alien -->
        <!-- <div v-if="sceltaUtente == 'Alien'" class="row flex-wrap justify-content-between">

            <div v-for="card in dataCard" class="card bg-warning p-0 mb-3" id="singleCard">
                <img :src="card.card_images[0].image_url" class="card-img-top" alt="">
                <div class="p-0">
                    <p class="card-text text-white text-center">{{ card.name.toUpperCase() }}</p>
                    <p class="card-text text-center">{{ card.archetype }}</p>
                </div>
            </div>

        </div> -->
        <!-- PRENDO I DATI DA AXIOS -->
        <!-- <pre class="bg-danger">{{ store.card }}</pre> -->

        <div class="row flex-wrap justify-content-between">

            <div v-for="card in store.card" v-show="card.archetype == sceltaUtente" class="card bg-warning p-0 mb-3"
                id="singleCard">
                <img :src="card.card_images[0].image_url" class="card-img-top" alt="">
                <div class="p-0">
                    <p class="card-text text-white text-center">{{ card.name.toUpperCase() }}</p>
                    <p class="card-text text-center">{{ card.archetype }}</p>
                </div>
            </div>

        </div>
        <!-- altrimenti mostro tutto -->
        <!-- <div v-esle class="row flex-wrap justify-content-between">

            <div v-for="card in dataCard" class="card bg-warning p-0 mb-3" id="singleCard">
                <img :src="card.card_images[0].image_url" class="card-img-top" alt="">
                <div class="p-0">
                    <p class="card-text text-white text-center">{{ card.name.toUpperCase() }}</p>
                    <p class="card-text text-center">{{ card.archetype }}</p>
                </div>
            </div>

        </div> -->

        <!-- <pre class="text-dark">{{ dataCard }}</pre> -->
    </section>
</template>

<style scoped>
#singleCard {
    width: 10rem;
}
</style>
