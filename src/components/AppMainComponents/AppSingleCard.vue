<script>
export default {
    props: {
        parts: Object
    },
    components: {

    },
    data() {
        return {

        }
    },
}
</script>

<template>
    <div class="card bg-warning p-0 mb-3" id="singleCard">
        <img :src="parts.card_images[0].image_url" class="card-img-top" alt="">
        <div class="p-0">
            <p class="card-text text-white text-center">{{ parts.name.toUpperCase() }}</p>
            <p class="card-text text-center">{{ parts.archetype }}</p>
        </div>
    </div>
</template>

<style scoped>
#singleCard {
    width: calc((100% / 5) - 1rem);
    margin: 0.5rem
}
</style>