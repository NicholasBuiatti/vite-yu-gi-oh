<script>
import dataCard from "../../data/dataCard.js";
import store from "../../data/store.js";
export default {
    props: {

    },
    components: {

    },
    data() {
        return {
            dataCard,
            store,
            archetypeInput: "seleziona",
            archetypeSelect: '',
        }
    },
    methods: {
        archetypeSelected(index) {
            this.archetypeSelect = this.store.allArchetypes[index].archetype_name;
            this.archetypeInput = this.archetypeSelect
            // console.log(this.archetypeSelect);
        },
    },
}
</script>

<template>
    <div class="dropdown p-2">
        <div v:model="archetypeInput" class="btn bg-white dropdown-toggle" data-bs-toggle="dropdown"
            aria-expanded="false">
            {{ archetypeInput }}
        </div>
        <ul class="dropdown-menu">
            <li v-for="archetype, i in this.store.allArchetypes" v:model="archetypeSelect"
                @click="archetypeSelected(i)">
                {{
                    archetype.archetype_name
                }}</li>
        </ul>

    </div>
    <div v:model="archetypeInput"> {{ archetypeInput }}</div>
</template>

<style scoped></style>