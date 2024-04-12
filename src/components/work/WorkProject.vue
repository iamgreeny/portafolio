<script setup>
const props = defineProps({
  project: {
    type: Object,
  },
});
</script>
<template>
  <div class="card" :class="project.img.length > 1 ? 'span2' : ''">
    <div class="image_wrapper">
      <img v-for="img in project.img" v-if="project.img" :src="img" alt="" />
    </div>
    <div class="card-text">
      <h2>{{ project.nombre }}</h2>
    </div>
  </div>
</template>

<style scoped>
.card {
  border: 1px solid black;
}

.image_wrapper {
  display: flex;
}

.span3 {
  grid-column: span 3;
}

.span3 .image_wrapper > img {
  width: 33.33%;
}

.span2 {
  grid-column: span 2;
}

.span2 .image_wrapper > img {
  width: 33.33%;
}

.image_wrapper > img {
  width: 100%;
  object-fit: cover;
}
</style>
