<script setup>
const props = defineProps({
  products: Array,
})


</script>

<template>
  <div class="products-list">
    <ul>
      <li v-for="product in products" :key="product.title">
        <div>{{ product.title }}</div>
        <div>{{ product.description }}</div>
        <div>{{ product.category }}</div>
        <div>{{ product.price }}</div>
      </li>
    </ul>
  </div>
</template>

<style>
.products-list {
  height: 800px;
  width: 700px;
  background-color: rgb(255, 255, 255);
}
</style>