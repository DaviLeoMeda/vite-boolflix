<script>
import MovieArea from './MovieArea.vue'

export default {
    name: "MainComp",
    components: {
        MovieArea
    }
}
</script>

<template>
    <main>
        <MovieArea />
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

main {
    background-color: $bg-sand;

    div {
        justify-content: center;
    }
}
</style>