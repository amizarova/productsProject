<script setup>
import FormOrder from './components/FormOrder/FormOrder.vue';
import ProductsList from './components/ProductsList.vue';
import { ref } from 'vue';

const products = ref([])
function addProduct(data) {
  products.value.push(data)
  console.log(data)
}
</script>

<template>
  <div class="layout">
    <ProductsList :products="products">

    </ProductsList>
    <FormOrder @collect="addProduct">

    </FormOrder>
  </div>
</template>

<style>
.layout {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 20px;
  background-color: rgb(255, 222, 200);
  gap: 30px;
}
</style>
