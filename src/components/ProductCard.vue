<script setup>
import { inject } from 'vue';

defineProps({
  imgPath: String,
  title: String,
  price: Number,
  isLiked: Boolean,
  isAdded: Boolean,
  id: Number,
})

const addToFavorite = inject('addToFavorite')
</script>

<template>
  <article
    class="relative flex flex-col gap-2 md:gap-3 w-full px-4 md:px-8 py-2 md:py-4 bg-white text-left rounded-2xl lg:rounded-3xl border border-gray-200 cursor-pointer transition hover:-translate-y-2 hover:shadow-xl"
  >
    <div class="relative self-center h-28 w-28 md:w-33 overflow-hidden">
      <img :src="imgPath" alt="Sneakers pair" class="h-auto w-full absolute bottom-0" />
    </div>
    <h3 class="text-xs md:text-sm">{{ title }}</h3>
    <div class="flex justify-between mt-auto">
      <div nt>
        <span class="text-xs text-gray-400 uppercase">цена:</span>
        <strong class="block text-sm">{{ price }}$</strong>
      </div>
      <img src="/plus.svg" alt="Plus" />
    </div>
    <img :src="isLiked ? '/like-2.svg' : '/like-1.svg'" alt="Like" @click="addToFavorite(id)" class="absolute w-8 h-8" />
  </article>
</template>
