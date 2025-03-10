<script setup>
import ProductCard from './ProductCard.vue';

const props = defineProps(["productCards"])

const { productCards } = props
</script>


<template>
  <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 mt-10 gap-2 md:gap-4">
    <ProductCard v-for="(_, index) in productCards" :key="index" />
  </div>
</template>
