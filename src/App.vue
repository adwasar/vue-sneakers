<script setup>
import { provide, ref } from 'vue'

import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'

const productCards = ref([
  {
    imgPath: '/sneakers/sneakers-1.jpg',
    title: 'Мужские Кроссовки Nike Blazer Mid Suede',
    price: 129,
    isLiked: false,
    isAdded: false,
    id: 0,
  },
  {
    imgPath: '/sneakers/sneakers-2.jpg',
    title: 'Мужские Кроссовки Nike Air Max 270',
    price: 129,
    isLiked: false,
    isAdded: false,
    id: 1,
  },
  {
    imgPath: '/sneakers/sneakers-3.jpg',
    title: 'Мужские Кроссовки Nike Blazer Mid Suede',
    price: 84,
    isLiked: false,
    isAdded: false,
    id: 2,
  },
  {
    imgPath: '/sneakers/sneakers-4.jpg',
    title: 'Кроссовки Puma X Aka Boku Future Rider',
    price: 89,
    isLiked: false,
    isAdded: false,
    id: 3,
  },
  {
    imgPath: '/sneakers/sneakers-5.jpg',
    title: 'Мужские Кроссовки Under Armour Curry 8',
    price: 151,
    isLiked: false,
    isAdded: false,
    id: 4,
  },
  {
    imgPath: '/sneakers/sneakers-6.jpg',
    title: 'Мужские Кроссовки Nike Kyrie 7',
    price: 107,
    isLiked: false,
    isAdded: false,
    id: 5,
  },
  {
    imgPath: '/sneakers/sneakers-7.jpg',
    title: 'Мужские Кроссовки Jordan Air Jordan 11',
    price: 107,
    isLiked: false,
    isAdded: false,
    id: 6,
  },
  {
    imgPath: '/sneakers/sneakers-8.jpg',
    title: 'Мужские Кроссовки Nike LeBron XVIII',
    price: 164,
    isLiked: false,
    isAdded: false,
    id: 7,
  },
  {
    imgPath: '/sneakers/sneakers-9.jpg',
    title: 'Мужские Кроссовки Nike Lebron XVIII Low',
    price: 139,
    isLiked: false,
    isAdded: false,
    id: 8,
  },
  {
    imgPath: '/sneakers/sneakers-10.jpg',
    title: 'Мужские Кроссовки Nike Blazer Mid Suede',
    price: 84,
    isLiked: false,
    isAdded: false,
    id: 9,
  },
  {
    imgPath: '/sneakers/sneakers-11.jpg',
    title: 'Кроссовки Puma X Aka Boku Future Rider',
    price: 89,
    isLiked: false,
    isAdded: false,
    id: 10,
  },
  {
    imgPath: '/sneakers/sneakers-12.jpg',
    title: 'Кроссовки Puma X Aka Boku Future Rider',
    price: 112,
    isLiked: false,
    isAdded: false,
    id: 11,
  },
])

const addToFavorite = (id) => {
  const item = productCards.value.find((item) => item.id === id)
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
      <CardList :productCards="productCards" />
    </section>
  </div>
</template>
