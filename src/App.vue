<script lang="ts" setup>
import { ref } from 'vue';

const title = ref('Hello, world!'); // Reactivity!

const wasAccepted = ref(false);
</script>

<template>
  <h1>{{ title }}</h1>

  <p v-if="wasAccepted">Accepted</p>
  <p v-else>Not accepted</p>

  <input v-model="wasAccepted" type="checkbox" />
</template>

<style scoped></style>
