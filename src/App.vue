<script setup>
import CartIcon from './components/icons/CartIcon.vue';
import HeartIcon from './components/icons/HeartIcon.vue';
import ProfileIcon from './components/icons/ProfileIcon.vue';
</script>

<template>
  <div class="w-5/6 max-w-5xl mx-auto my-20 bg-white drop-shadow-md rounded-2xl">

    <header
      class="flex justify-between gap-x-4 md:gap-x-6 xl:gap-x-8 px-8 md:px-12 xl:px-16 py-4 md:py-6 xl:py-8 border-b border-[#EAEAEA]">
      <div class="flex justify-between items-center gap-x-2 md:gap-x-4">
        <img class="w-8 md:w-10 h-8 md:h-10" src="/logo.png" alt="logo">
        <div>
          <h1 class="text-sm md:text-lg xl:text-xl font-bold">VUE SNEAKERS</h1>
          <p class="text-[8px] md:text-sm text-[#9D9D9D]">Магазин лучших кроссовок</p>
        </div>
      </div>

      <ul class="flex gap-x-4 md:gap-x-6 xl:gap-x-8">
        <li class="flex items-center gap-x-2 cursor-pointer text-[#5C5C5C] font-semibold hover:text-black">
          <CartIcon />
          <span class="hidden xl:inline">600&nbsp;грн</span>
        </li>
        <li class="flex items-center gap-x-2 cursor-pointer text-[#5C5C5C] hover:text-black">
          <HeartIcon />
          <span class="hidden xl:inline">Закладки</span>
        </li>
        <li class="flex items-center gap-x-2 cursor-pointer text-[#5C5C5C] hover:text-black">
          <ProfileIcon />
          <span class="hidden xl:inline">Профиль</span>
        </li>
      </ul>
    </header>

    <section class="px-15 py-11">
      <h1 class="text-3xl font-bold underline">Hello vue</h1>
    </section>

  </div>
</template>