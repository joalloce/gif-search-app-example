<template>
  <div class="navbar">
    <p>Gif Search Demo</p> 
    <Search @fetch-gifs="$emit('gifs-data',$event)"/>
  </div>
</template>

<script setup>
import Search from './Search.vue'

</script>

<style>
.navbar {
  display: flex;
  flex-direction: column;
}
p {
  font-size: 25px;
}
</style>