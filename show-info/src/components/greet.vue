<script setup lang="ts">
import {ref} from "vue";
import { invoke } from "@tauri-apps/api/core";

const greetMsg = ref("");
const name = ref("");

async function greet() {
  greetMsg.value = await invoke("greet", { name: name.value });
}

</script>

<template>
  <div>
    <form class="my-3" @submit.prevent="greet">
      <input class="shadow appearance-none border rounded py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="greet-input" v-model="name" placeholder="Enter a name..." />
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold ml-2 py-2 px-3 rounded" type="submit">Greet</button>
    </form>
    <p class="text-center text-black">{{ greetMsg }}</p>
  </div>
</template>

<style scoped lang="scss">

</style>