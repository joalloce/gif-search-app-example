<script setup>
import Navbar from './components/Navbar.vue';
import GifList from './components/GifList.vue';

import { ref } from "vue"
const gifs = ref([]);

function onData(data) {
  gifs.value = data;
}

</script>

<template>
  <Navbar @gifs-data="onData"/>
  <GifList :gifs="gifs"/>
</template>

<style scoped>
* { 
  box-sizing: border-box;
}
</style>
