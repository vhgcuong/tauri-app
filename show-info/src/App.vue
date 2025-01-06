<script setup lang="ts">
import Greet from "./components/greet.vue";
import Welcome from "./components/welcome.vue";
import Count from "./components/count.vue";
</script>

<template>
  <main class="mt-8 container mx-auto text-center">
    <welcome />
    <greet />
    <count />
  </main>
</template>

<style lang="scss">
@use "scss/main.scss";
</style>