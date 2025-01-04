<script setup lang="ts">
import Greet from "./components/greet.vue";
import Welcome from "./components/welcome.vue";
</script>

<template>
  <main class="mt-8 container mx-auto text-center">
    <welcome />
    <greet />
  </main>
</template>

<style lang="scss">
@use "scss/main.scss";
</style>