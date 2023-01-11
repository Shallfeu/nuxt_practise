<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4">
        <nuxt-link to="/" class="font-bold">Nuxt Power</nuxt-link>
      </nav>
    </header>

    <div class="container mx-auto p-4">
      <slot></slot>
    </div>

    <footer class="container mx-auto p-4 border-t-2">
      <ul class="flex justify-between">
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about">About</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/products">Products</nuxt-link>
        </li>
      </ul>
    </footer>
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: teal;
}
</style>
