<script setup lang="ts">
import {ref} from 'vue'

const count = ref(0)

</script>

<template>
  <div class="flex justify-center items-center flex-col">
    <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold ml-2 w-full rounded" @click="count++">+</button>
    <div class="flex justify-center mx-1 my-1">
      Count is: {{ count }}
    </div>
    <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold ml-2 w-full rounded" @click="--count">-</button>
  </div>
</template>

<style scoped lang="scss">

</style>