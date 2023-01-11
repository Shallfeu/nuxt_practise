<template>
  <div class="card flex flex-col items-center p-8">
    <img :src="product.image" alt="product-image" class="w-32 h-48 mb-4" />
    <p class="font-bold text-gray-500 mb-4 truncate">{{ product.title }}</p>
    <button type="button" class="btn mt-auto w-full">
      <nuxt-link :to="`/products/${product.id}`">View Detail</nuxt-link>
    </button>
  </div>
</template>

<script setup>
const { product } = defineProps(['product']);
</script>

<style scoped>
img {
  width: 200px;
}
</style>
