<script setup>
import { proyectos } from "@/database/proyectos.js";
import WorkProject from "@/components/work/WorkProject.vue";
</script>

<template>
  <section>
    <img class="nubecolor" src="/images/work/nubes_arriba.svg" alt="" />

    <div class="container">
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
.container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 80%;
  gap: 1rem;
}
</style>
