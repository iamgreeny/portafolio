<script setup>
import { proyectos } from "@/database/proyectos.js";
import WorkProject from "@/components/work/WorkProject.vue";
</script>

<template>
  <section>
    <img class="nubecolor" src="/images/work/nubes_arriba.svg" alt="" />
    <div class="container">
      <h1 class="centered">Art Collection</h1>
      <WorkProject
        v-for="project in proyectos"
        :key="project.id"
        :project="project"
      />
    </div>

    <img class="nubemorada" src="/images/work/nubes_abajo.svg" alt="" />
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
}
h1 {
  font-size: 7rem;
  color: #29235c;
  font-family: gilroy_regular;
  font-weight: 100;
  text-align: center;
}

.centered {
  grid-column: 1/-1;
  font-family: kaoly_font;
}

.nubecolor {
  position: absolute;
}
.container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 80%;
  gap: 1rem;
  margin-top: 35%;
}

@media screen and (max-width: 800px) {
  .container {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>
