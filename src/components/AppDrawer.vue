<script setup>
import { inject, computed } from 'vue'

const closeCart = inject('closeCart')
const cards = inject('cards')
const addedToCartCards = computed(() => {
  return cards.value.filter((card) => card.isAddedToCart === true)
})

</script>

<template>
  <div class="absolute w-100 right-0 h-full bg-white">
    <button class="absolute right-0 w-16 h-16 bg-red-800 cursor-pointer" @click="closeCart()">
      X
    </button>
    <div class="mt-20">
      {{ addedToCartCards }}
    </div>
  </div>
</template>
