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
      <h1>{{ project.nombre }}</h1>
      <h2>{{ `${project.categoria} ${project.tecnica}` }}</h2>
    </div>
  </div>
</template>

<style scoped>
.card {
  border: 1px solid black;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  background-color: var(--color-primary);
  border-radius: 25px;
  padding: 1rem;
}

.card-text {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.card-text > * {
  text-align: center;
  color: var(--color-accent);
  text-transform: capitalize;
}

.image_wrapper {
  display: flex;
  width: 100%;
}

.span2 .image_wrapper > img {
  width: 33.33%;
}

.image_wrapper > img {
  width: 100%;
  object-fit: cover;
  border-radius: 15px;
}

@media screen and (max-width: 800px) {
  .span2,
  .span3 {
    grid-column: span 1 !important;
  }

  .image_wrapper {
    flex-direction: column;
  }

  .span2 .image_wrapper > img {
    width: 100%;
  }
}
</style>
