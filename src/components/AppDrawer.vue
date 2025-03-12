<script setup>
import { inject, computed } from 'vue'

import DrawerCard from './DrawerCard.vue'

const closeCart = inject('closeCart')
const cards = inject('cards')
const addedToCartCards = computed(() => {
  return cards.value.filter((card) => card.isAddedToCart === true)
})
</script>

<template>
  <div class="absolute w-full sm:w-100 xl:w-120 right-0 h-full bg-white overflow-auto">
    <button class="absolute right-0 w-12 h-12 bg-red-800 cursor-pointer" @click="closeCart()">
      X
    </button>
    <div class="flex flex-col gap-5 px-4 md:px-8 xl:px-16 py-10 md:py-16 xl:py-22">
      <DrawerCard
        v-for="card in addedToCartCards"
        :key="card.id"
        :imgPath="card.imgPath"
        :title="card.title"
        :price="card.price"
        :id="card.id"
      />
    </div>
  </div>
</template>
