<script>
import dataCard from "../../data/dataCard.js";
export default {
    props: {

    },
    components: {

    },
    data() {
        return {

            dataCard
        }
    },
    methods: {
        archetypeSelected() {

        },
    },
}
</script>

<template>
    <div class="dropdown p-2">
        <button class="btn bg-white dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            Select archetype
        </button>
        <ul class="dropdown-menu">
            <li v-for="card in dataCard">{{ card.archetype }}</li>
        </ul>
    </div>
</template>

<style scoped></style>