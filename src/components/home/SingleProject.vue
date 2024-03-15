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
    </div>
    <img src="/images/home/category_frame.svg" alt="Project Image" />
  </div>
</template>

<style scoped>
.card {
  /* Add your card styles here */
}
.card-text {
  position: absolute;
  width: 50%;
  left: 10%;
  bottom: 10%;
  z-index: 1;
}
</style>
