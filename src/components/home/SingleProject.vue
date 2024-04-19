<script setup>
import { defineProps } from "vue";
import { proyectos } from "@/database/proyectos.js";
import { useRouter } from "vue-router";

const router = useRouter();
const navigateTo = (path) => {
  router.push(path);
};

const props = defineProps({
  projectIndex: {
    type: Number,
  },
});
</script>
<template>
  <div class="card" @click="navigateTo('/work')">
    <div class="card-text">
      <h2>{{ proyectos[projectIndex].nombre }}</h2>
    </div>
    <img src="/images/home/category_frame.svg" alt="Project Image" />
    <div id="project_image_cont">
      <img :src="proyectos[projectIndex].img[0]" alt="" />
    </div>
  </div>
</template>

<style scoped>
.card {
  /* Add your card styles here */
  cursor: pointer;
}
.card-text {
  position: absolute;
  width: 50%;
  left: 10%;
  bottom: 10%;
  z-index: 1;
  text-transform: capitalize;
}

#project_image_cont {
  position: absolute;
  top: 5%;
  width: 90%;
  left: 3%;
  height: 66%;

  border-radius: 28px;
  overflow: hidden;

  img {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: cover;
  }
}
</style>
