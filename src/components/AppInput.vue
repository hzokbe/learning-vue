<script lang="ts" setup>
const model = defineModel();

interface Props {
  placeholder: string;

  required: boolean;

  type: 'text' | 'number';
}

defineProps<Props>();
</script>

<template>
  <input v-model="model" :placeholder="placeholder" :required="required" :type="type" />
</template>

<style scoped>
input {
  padding: 0.5rem 1rem;

  border-radius: 0.2rem;

  border: solid #e5e5e5 1px;

  outline: none;

  color: #0a0a0a;
}
</style>
