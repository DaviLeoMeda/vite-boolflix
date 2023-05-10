<script>
import MovieCard from './MovieCard.vue'
import { store } from "../store"

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
    methods() {

    }
}
</script>

<template>
    <div class="inserting d-flex p-5">
        <input type="text" placeholder="Select your favorite Movie or Serie">
        <button>Send</button>
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