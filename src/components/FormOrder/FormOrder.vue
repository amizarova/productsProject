<script setup>
import ProductsForm from './ProductsForm.vue';
import ProductsOrder from './ProductsOrder.vue';

const emit = defineEmits(['collect'])

</script>

<template>
  <div class="form-order">
    <ProductsForm @collect="$emit('collect', $event)">

    </ProductsForm>
    <ProductsOrder>

    </ProductsOrder>
  </div>
</template>

<style>
.form-order {
  width: 300px;
  height: 800px;
  background-color: rgb(255, 255, 255);
}
</style>