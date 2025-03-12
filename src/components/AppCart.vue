<script setup>
import AppDrawer from './AppDrawer.vue';

defineProps({
  cartIsOpen: Boolean
})
</script>

<template>
  <div v-show="cartIsOpen" class="fixed top-0 right-0 bottom-0 left-0 bg-black/25 ">
    <AppDrawer />
  </div>
</template>
