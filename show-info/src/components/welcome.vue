<script setup lang="ts">

import {invoke} from "@tauri-apps/api/core";
import {onMounted, ref} from "vue";

const welcomeMsg = ref("");

async function welcome() {
  welcomeMsg.value = await invoke("welcome");
}

onMounted(() => {
  welcome();
})
</script>

<template>
  <h1 class="text-3xl font-bold">{{ welcomeMsg }}</h1>
</template>

<style scoped lang="scss">

</style>