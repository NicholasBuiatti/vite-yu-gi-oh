<script>
import AppMainCard from "./AppMainCard.vue"
export default {
    components: {
        AppMainCard,
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <section class="container bg-white p-3">
        <div class="bg-dark text-white">
            <h5>Found 39 cards</h5>
            <!-- qua ci va un ciclo v-for con le carte -->
            <AppMainCard />
        </div>
    </section>
</template>

<style scoped></style>