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
    <h2>Titulo del Proyecto</h2>
    <h3>Subtitulo del Proyecto</h3>
    <img src="" alt="Project Image" />
  </div>
</template>

<style scoped>
.card {
  /* Add your card styles here */
}
</style>
