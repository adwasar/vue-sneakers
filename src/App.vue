<script setup>
import { provide, ref } from 'vue'

import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
import AppCart from './components/AppCart.vue'

import { productCards } from './data/productCards.json'

const cards = ref(productCards)
const cartIsOpen = ref(false)

const addToFavorite = (id) => {
  const item = cards.value.find((item) => item.id === id)
  if (item) {
    item.isLiked = !item.isLiked
  }
}

const addToСart = (id) => {
  const item = cards.value.find((item) => item.id === id)
  if (item) {
    item.isAddedToCart = !item.isAddedToCart
  }
}

const openCart = () => {
  cartIsOpen.value = true
  document.body.classList.add("overflow-hidden")
}

const closeCart = () => {
  cartIsOpen.value = false
  document.body.classList.remove("overflow-hidden")
}

provide('addToFavorite', addToFavorite)
provide('addToСart', addToСart)
provide('closeCart', closeCart)
</script>

<template>
  <div class="w-11/12 max-w-5xl mx-auto my-20 bg-white drop-shadow-md rounded-2xl">
    <AppHeader @openCart="openCart" />

    <section class="px-4 md:px-8 xl:px-16 py-10 md:py-16 xl:py-22">
      <h2 class="text-xl font-bold md:text-3xl">Все кроссовки</h2>
      <CardList :cards="cards" />
    </section>
  </div>
  <AppCart :cartIsOpen="cartIsOpen" />
</template>
