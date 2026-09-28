<script lang="ts" setup>
import { ref } from 'vue';

const title = ref('Hello, world!'); // Reactivity!

const users = ref([
  {
    id: 1,
    username: 'kaguya_shinomiya',
  },
  {
    id: 2,
    username: 'miyuki_shirogane',
  },
]);
</script>

<template>
  <h1>{{ title }}</h1>
  <ul>
    <li v-for="user in users" :key="user.id">{{ user.id }}: {{ user.username }}</li>
  </ul>
</template>

<style scoped></style>
