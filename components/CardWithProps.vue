<script setup lang="ts">
const props = defineProps<{
  title: string;
  imageUrl: string;
  description: string;
}>();
</script>

<template>
  <div :class="styles.root">
    <h3>{{ props.title }}</h3>
    <img :src="props.imageUrl" width="200" height="200" />
    <p>{{ props.description }}</p>
  </div>
</template>

<style module="styles">
.root {
  display: flex;
  flex-direction: column;
  width: 300px;
  padding: 32px;
  background-color: lightyellow;
  border-radius: 6px;
}
</style>
