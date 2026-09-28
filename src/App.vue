<script lang="ts" setup>
import { ref } from 'vue';

const title = ref('Hello, world!'); // Reactivity!
</script>

<template>
  <h1>{{ title }}</h1>

  <input v-model="title" placeholder="Enter a title" />
</template>

<style scoped></style>
