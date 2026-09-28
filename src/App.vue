<script lang="ts" setup>
import { ref } from 'vue';

const title = ref('Hello, world!'); // Reactivity!

const description = ref('Lorem ipsum dolor sit amet');

const showDescription = ref(false);
</script>

<template>
  <h1>{{ title }}</h1>
  <p v-if="showDescription">{{ description }}</p>
</template>

<style scoped></style>
