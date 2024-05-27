<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import dataCard from "./data/dataCard.js";
import store from "./data/store.js";
export default {
    components: {
        AppHeader,
        AppMain,
    },
    data() {
        return {
            dataCard,
            store,
        }
    },
    created() {
        axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0").then(risultato => {
            // this.store.personaggi = risultato.data.results;
            console.log(risultato.data);

            this.store.card = risultato.data.data
            console.log(this.store);
        });
    },
    mounted() {

    }
}
</script>

<template>
    <section class="container">
        <AppHeader />
        <AppMain />
    </section>
</template>

<style scoped></style>
