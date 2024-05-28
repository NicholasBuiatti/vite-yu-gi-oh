<script>
import AppMainCards from "./AppMainCards.vue";
import store from "../../data/store.js"
export default {
    components: {
        AppMainCards,
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
            <AppMainCards />
        </div>
    </section>
</template>

<style scoped></style>