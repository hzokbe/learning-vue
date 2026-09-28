<script lang="ts" setup>
import { computed, ref } from 'vue';

const title = ref('Hello, world!'); // Reactivity!

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
</script>

<template>
  <h1>{{ title }}</h1>
  <p>Total price: US$ {{ totalPrice }}</p>
</template>

<style scoped></style>
