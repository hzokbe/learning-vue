<script lang="ts" setup>
interface Props {
  type: 'button' | 'submit';

  variant: 'ghost' | 'danger';
}

defineProps<Props>();

interface Emits {
  click: [event: MouseEvent];
}

const emit = defineEmits<Emits>();

const onClick = (event: MouseEvent) => emit('click', event);
</script>

<template>
  <button :class="['button', variant]" :type="type" @click="onClick">
    <slot />
  </button>
</template>

<style scoped>
button {
  padding: 0.5rem 1rem;

  cursor: pointer;

  border: none;

  border-radius: 0.2rem;

  color: #fafafa;

  font-weight: bolder;
}

.ghost {
  border-color: #e5e5e5;

  background-color: #fafafa;

  color: #0a0a0a;
}

.danger {
  background-color: #ef4444;
}
</style>
