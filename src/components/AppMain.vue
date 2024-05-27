<script>
import AppMainButtonSearch from "./AppMainComponents/AppMainButtonSearch.vue";
import AppMainContainerSearch from "./AppMainComponents/AppMainContainerSearch.vue";
export default {
    components: {
        AppMainButtonSearch,
        AppMainContainerSearch,
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <section class="container bg-warning p-4">
        <AppMainButtonSearch />
        <AppMainContainerSearch />
    </section>
</template>

<style scoped></style>