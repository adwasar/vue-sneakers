<script setup>
defineProps({
  title: String,
  imgPath: String,
  price: Number,
  id: Number
})
</script>

<template>
  <article
    class="flex items-center gap-2 md:gap-3 w-full max-w-md mx-auto px-4 md:px-8 py-2 md:py-4 bg-white text-left rounded-2xl lg:rounded-3xl border border-gray-200 transition hover:-translate-y-2 hover:shadow-xl"
  >
    <div class="flex items-center self-center w-18 h-18 md:w-33 overflow-hidden">
      <img :src="imgPath" alt="Sneakers pair" class="w-full h-auto " />
    </div>
    <div>
      <h3 class="text-xs md:text-sm">{{ title }}</h3>
      <div class="flex justify-between mt-auto">
        <div>
          <strong class="block text-sm">{{ price }}$</strong>
        </div>
      </div>
    </div>
    <img src="/close.svg" alt="Close" class="w-8 h-8 self-end cursor-pointer ml-auto">
  </article>
</template>
