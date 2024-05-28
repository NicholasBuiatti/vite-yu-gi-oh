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
        // TENGO IN CONSIDERAZIONE IN BASE ALL'INDEX LA SCELTA CHE FACCIO COME INPUT
        archetypeSelected(index) {
            this.archetypeSelect = this.store.allArchetypes[index].archetype_name;
            this.archetypeInput = this.archetypeSelect
            // console.log(this.archetypeSelect);
            axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${this.archetypeSelect}`).then(risultato => {
                this.store.card = risultato.data.data
            });
        },
        // IMPOSTO LA RICERCA DIRETTAMENTE SULLA CHIAMATA AL SERVER
        // search() {
        //     axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${this.archetypeSelect}`).then(risultato => {
        //         this.store.card = risultato.data.data
        //     });
        // },
    },
}
</script>

<template>
    <div class="dropdown p-2">
        <div v:model="archetypeInput" class="btn bg-white dropdown-toggle" data-bs-toggle="dropdown"
            aria-expanded="false">
            {{ archetypeInput }}
        </div>
        <ul class="dropdown-menu overflow-auto">
            <li v-for="archetype, i in this.store.allArchetypes" v:model="archetypeSelect"
                @click="archetypeSelected(i)">
                {{
                    archetype.archetype_name
                }}</li>
        </ul>

    </div>
    <!-- <button @click="search">Search</button> -->
</template>

<style scoped>
li {
    cursor: pointer;
}

.dropdown-menu {
    height: 20rem;
}
</style>