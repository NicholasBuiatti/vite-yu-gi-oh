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
    }
}
</script>

<template>
    <section class="container bg-white p-3">
        <div class="row justify-content-between">

            <div v-for="card in dataCard" class="card bg-warning p-0 mb-3">

                <img :src="card.card_images[0].image_url" class="card-img-top" alt="">
                <div class="card-body">
                    <p class="card-text">{{ card.name.toUpperCase() }}</p>
                </div>
                <!-- <pre class="text-dark">{{ card.card_images[0].image_url }}</pre> -->

            </div>
        </div>
        <!-- <pre class="text-dark">{{ dataCard }}</pre> -->
    </section>
</template>

<style scoped>
.card {
    width: 10rem;
}
</style>