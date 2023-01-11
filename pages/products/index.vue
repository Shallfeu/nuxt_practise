<template>
  <div v-if="products.length > 0" class="grid grid-cols-1 gap-5 sm:grid-cols-4">
    <ProductCard v-for="p in products" :product="p" />
  </div>
  <div v-else>We are running out of stock, sorry...</div>
</template>

<script setup>
const URL = 'https://fakestoreapi.com/products';

definePageMeta({
  layout: 'products',
});

const { data: products } = await useFetch(URL);

useHead({ title: 'Nuxt Power | Products', meta: [{ name: 'description', content: 'Products' }] });
</script>

<style scoped>
h2 {
  margin-top: 20px;
  font-size: 36px;
}

p {
  margin-top: 20px;
}
</style>
