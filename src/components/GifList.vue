<template>
  <gif v-for="gif in gifs" :key="gif.id" :gif="gif" />
</template>

<script>
import Gif from './Gif.vue'

export default {
  components: { Gif },
  props: {
    gifs: Array
  }

}
</script>

<style>

</style>