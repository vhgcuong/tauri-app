<script setup lang="ts">
import {ref} from 'vue'

const count = ref(0)
</script>

<template>
  <div class="h-full flex justify-center items-center">
    <button class="bg-gradient-to-r from-blue-300 to-blue-800" @click="count++">
      Count is: {{ count }}
    </button>
  </div>
</template>

<style scoped lang="scss">

</style>