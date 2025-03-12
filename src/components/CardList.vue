<script setup>
import ProductCard from './ProductCard.vue'

defineProps({
  cards: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 mt-10 gap-2 md:gap-4">
    <ProductCard
      v-for="(card, index) in cards"
      :key="index"
      :imgPath="card.imgPath"
      :title="card.title"
      :price="card.price"
      :isLiked="card.isLiked"
      :isAdded="card.isAdded"
      :id="card.id"
    />
  </div>
</template>
