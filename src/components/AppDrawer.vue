<script setup>
import { inject } from 'vue'

const closeCart = inject('closeCart')
</script>

<template>
  <div class="absolute w-100 right-0 h-full bg-white">
    <button class="absolute right-0 w-16 h-16 bg-red-800 cursor-pointer" @click="closeCart()">X</button>
  </div>
</template>
