<script setup>
import CartIcon from './icons/CartIcon.vue'
import HeartIcon from './icons/HeartIcon.vue'
import ProfileIcon from './icons/ProfileIcon.vue'
</script>

<template>
  <header
    class="flex justify-between gap-x-4 md:gap-x-6 xl:gap-x-8 px-4 md:px-8 xl:px-16 py-4 md:py-6 xl:py-8 border-b border-gray-200"
  >
    <div class="flex justify-between items-center gap-x-2 md:gap-x-4">
      <img class="w-8 md:w-10 h-8 md:h-10" src="/logo.png" alt="logo" />
      <div class="cursor-pointer">
        <h1 class="text-sm md:text-lg xl:text-xl font-bold">VUE SNEAKERS</h1>
        <p class="text-[8px] md:text-sm text-gray-400">Магазин лучших кроссовок</p>
      </div>
    </div>

    <ul class="flex gap-x-4 md:gap-x-6 xl:gap-x-8">
      <li
        class="flex items-center gap-x-2 cursor-pointer text-gray-600 font-semibold hover:text-black"
      >
        <CartIcon />
        <span class="hidden xl:inline">600&nbsp;грн</span>
      </li>
      <li class="flex items-center gap-x-2 cursor-pointer text-gray-600 hover:text-black">
        <HeartIcon />
        <span class="hidden xl:inline">Закладки</span>
      </li>
      <li class="flex items-center gap-x-2 cursor-pointer text-gray-600 hover:text-black">
        <ProfileIcon />
        <span class="hidden xl:inline">Профиль</span>
      </li>
    </ul>
  </header>
</template>
