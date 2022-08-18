<script setup>
import Navbar from './components/Navbar.vue';
import GifList from './components/GifList.vue';

const gifs = ref([]);

</script>

<template>
<Navbar />
<GifList :gifs="gifs"/>

</template>

<style scoped>
</style>
