<script setup>
import { ref } from 'vue';

const emit = defineEmits(['collect'])


const product = ref({
  title: '',
  description: '',
  price: '',
  category: '',
})
function dataCollector() {
  emit('collect', {...product.value})
  product.value.title = ''
  product.value.description = ''
  product.value.price = ''
  product.value.category = ''
}
</script>

<template>
  <div class="products-form">
    <input v-model="product.title" type="text" placeholder="Введите название товара">
    <input v-model="product.description" type="text" placeholder="Введите описание товара">
    <input v-model="product.price" type="text" placeholder="Введите цену товара">
    <input v-model="product.category" type="text" placeholder="Введите категорию товара">
    <button @click="dataCollector">Добавить продукт</button>
  </div>
</template>

<style>
.products-form {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 10px;
  border: 2px solid black;
  padding: 20px;
}
</style>