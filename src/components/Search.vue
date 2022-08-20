<template>
  <div class="search">
    <input placeholder="Search GIF" v-model="keyword">
    <button @click="onClick">Search</button>
  </div>
</template>

<script setup>
import { ref } from "vue"

const keyword = ref("")

const emit = defineEmits(["fetch-gifs"])

function onClick(e) {
  e.preventDefault();
  fetch(`https://api.giphy.com/v1/gifs/search?api_key=${import.meta.env.VITE_API_KEY}&q=${keyword.value}&limit=20`)
    .then(res => res.json())
    .then(json => {
      emit("fetch-gifs", json.data)
    })

}

</script>

<style>
  button {
    width: 30%;
    margin-left: 20px;
    border: 1.5px solid;
    background-color: lightgreen;
    cursor: pointer;
    font-size: 16px;
  }

  input {
    padding: 10px 10px;
    outline: 0;
    font-size: 16px;
    border: 1.5px solid black;
    width: 70%;
    display: block;
  }

  input:focus {
    border-color: blueviolet;
  }

  .search {
    display: flex;
    width: 100%;
    
  }
</style>