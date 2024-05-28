<script>
import AppSingleCard from "./AppSingleCard.vue";
import dataCard from "../../data/dataCard.js";
import store from "../../data/store.js";
export default {
    props: {

    },
    components: {
        AppSingleCard
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
        <!-- PRENDO I DATI DA AXIOS -->
        <div class="row flex-wrap">
            <AppSingleCard v-for="card in store.card" :parts='card' />
        </div>
        <!-- <pre class="text-dark">{{ dataCard }}</pre> -->
    </section>
</template>

<style scoped></style>
