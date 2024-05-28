<script>
import AppMainCard from "./AppMainCard.vue";
import store from "../../data/store.js"
export default {
    components: {
        AppMainCard,
    },
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <section class="container bg-white p-3">
        <div class="bg-dark text-white">
            <h5>Found {{ store.card.length }} cards</h5>
            <!-- qua ci va un ciclo v-for con le carte -->
            <AppMainCard />
        </div>
    </section>
</template>

<style scoped></style>