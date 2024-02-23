<script setup>
import { RouterLink, RouterView } from "vue-router";
import TheHeader from "@/components/layouts/TheHeader.vue";
import TheFooter from "@/components/layouts/TheFooter.vue";
</script>

<template>
  <div>
    <TheHeader />
    <RouterView />
    <TheFooter />
  </div>
</template>

<style scoped>
.prueba {
  background-color: brown;
  height: 20px;
}
</style>
