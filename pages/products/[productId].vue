<template>
  <div>
    <Head>
      <Title>Nuxt Power | {{ product.title }}</Title>
      <Meta name="description" :content="product.description" />
    </Head>

    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
const { productId } = useRoute().params;

const URL = `https://fakestoreapi.com/products/${productId}`;

const { data: product } = await useFetch(URL, { key: productId });

if (!product.value) {
  throw createError({ statusCode: 404, statusMessage: 'Product Not Found', fatal: true });
}

definePageMeta({
  layout: 'products',
});
</script>

<style scoped>
h2 {
  margin-top: 20px;
  font-size: 36px;
}
</style>
