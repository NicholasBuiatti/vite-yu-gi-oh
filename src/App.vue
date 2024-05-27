<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
export default {
    components: {
        AppHeader,
        AppMain,
    },
    data() {
        return {

        }
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
