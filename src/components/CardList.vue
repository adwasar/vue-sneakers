<script setup>
import AppCard from './AppCard.vue'

defineProps({
  cards: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 mt-10 gap-2 md:gap-4">
    <AppCard
      v-for="card in cards"
      :key="card.id"
      :imgPath="card.imgPath"
      :title="card.title"
      :price="card.price"
      :isLiked="card.isLiked"
      :isAddedToCart="card.isAddedToCart"
      :id="card.id"
    />
  </div>
</template>
