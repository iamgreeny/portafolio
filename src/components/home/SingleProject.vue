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
    <div class="card-text">
      <h2>Titulo del Proyecto</h2>
      <h3>Subtitulo del Proyecto</h3>
    </div>
    <img src="/images/Modeling.jpg" alt="Project Image" />
  </div>
</template>

<style scoped>
.card {
  /* Add your card styles here */
}
.card-text {
  position: absolute;
  width: 40%;
  left: 42px;
  bottom: 47px;
  z-index: 1;
}
</style>
