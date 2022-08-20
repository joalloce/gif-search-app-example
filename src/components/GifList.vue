<template>
<div class="gif-list">
  <gif v-for="gif in gifs" :key="gif.id" :gif="gif" />
</div>
</template>

<script setup>
import Gif from './Gif.vue'

defineProps({
  gifs: Array
});

</script>

<style>
.gif-list {
  margin-top: 10px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>