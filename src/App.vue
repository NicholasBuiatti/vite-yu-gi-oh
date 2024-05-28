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
        axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=0&archetype=alien").then(risultato => {
            this.store.card = risultato.data.data
        });
        axios.get("https://db.ygoprodeck.com/api/v7/archetypes.php").then(risultato => {
            this.store.allArchetypes = risultato.data
            console.log(this.store.allArchetypes);
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
