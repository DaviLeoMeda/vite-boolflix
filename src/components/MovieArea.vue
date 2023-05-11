<script>
import MovieCard from './MovieCard.vue'
import { store } from "../store"
import axios from 'axios'

export default {
    name: "MovieArea",
    components: {
        MovieCard
    },
    data() {
        return {
            store
        }
    },

    crerated() {

    },
    methods: {

        APIcall() {
            axios.get(`https://api.themoviedb.org/3/search/movie?api_key=${store.api_key}&query=${store.searchText}`)
                .then((res) => {
                    store.arrayMovie = res.data.results
                })
        }
    }
}
</script>

<template>
    <div class="inserting d-flex p-5">
        <input type="text" placeholder="Select your favorite Movie or Serie" v-model="store.searchText">
        <button @click="APIcall">Search it!</button>
    </div>

    <MovieCard />
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


.inserting {
    input {
        width: 20rem;
    }
}

.bg-base {
    background-color: $bg-pinker;
}
</style>