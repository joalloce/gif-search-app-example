<template>
  <div class="gif" :style="`background-image: url(${gif.images.fixed_width_downsampled.url})`"></div>
</template> 

<script setup>
defineProps({
  gif: Object
});
</script>

<style>
.gif {
  margin: 10px;
  width: 200px;
  height: 200px;
  background-repeat: no-repeat;
}
</style>