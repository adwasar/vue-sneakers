<script setup>
import { provide, ref } from 'vue'

import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'

import { productCards } from './data/productCards.json'

const cards = ref(productCards)

const addToFavorite = (id) => {
  const item = cards.value.find((item) => item.id === id)
  if (item) {
    item.isLiked = !item.isLiked
  }
}

provide('addToFavorite', addToFavorite)
</script>

<template>
  <div class="w-11/12 max-w-5xl mx-auto my-20 bg-white drop-shadow-md rounded-2xl">
    <AppHeader />

    <section class="px-4 md:px-8 xl:px-16 py-10 md:py-16 xl:py-22">
      <h2 class="text-xl font-bold md:text-3xl">Все кроссовки</h2>
      <CardList :cards="cards" />
    </section>
  </div>
</template>
