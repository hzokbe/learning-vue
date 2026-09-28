<script lang="ts" setup>
import { computed, ref } from 'vue';

const title = ref('Hello, world!'); // Reactivity!

const productName = ref('');

const productPrice = ref(0.0);

const products = ref([
  {
    id: 1,
    name: 'Book',
    price: 5,
  },
  {
    id: 2,
    name: 'Notebook',
    price: 800,
  },
  {
    id: 3,
    name: 'Smartphone',
    price: 500,
  },
]);

const totalPrice = computed(() => {
  return products.value.reduce((sum, product) => sum + product.price, 0.0);
});

const onSubmit = (event: SubmitEvent) => {
  event.preventDefault();

  products.value.push({
    id: products.value.length,
    name: productName.value,
    price: productPrice.value,
  });

  productName.value = '';

  productPrice.value = 0.0;
};
</script>

<template>
  <h1>{{ title }}</h1>
  <p>Total price: US$ {{ totalPrice }}</p>
  <form @submit="onSubmit">
    <input v-model="productName" placeholder="Product name" />
    <input v-model="productPrice" placeholder="Product price" type="number" />
    <button type="submit">Add to cart</button>
  </form>
</template>

<style scoped></style>
