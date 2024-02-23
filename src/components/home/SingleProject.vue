<script setup>
import { defineProps } from "vue";

const props = defineProps({
  imageUrl: {
    type: String,
  },
  title: {
    type: String,
  },
  subtitle: {
    type: String,
  },
});
</script>
<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <h3>{{ subtitle }}</h3>
    <img :src="imageUrl" alt="Project Image" />
  </div>
</template>

<style scoped>
.card {
  /* Add your card styles here */
}
</style>
