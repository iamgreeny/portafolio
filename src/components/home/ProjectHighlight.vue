<script setup>
import SingleProject from "./SingleProject.vue";
</script>

<template>
  <section>
    <SingleProject />
    <SingleProject />
    <SingleProject />
  </section>
</template>

<style lang="scss" scoped>
section {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  margin-top: 2rem;
}
</style>
