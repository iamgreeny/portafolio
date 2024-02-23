<script setup>
import TheHero from "@/components/home/TheHero.vue";
import TextIntro from "@/components/home/TextIntro.vue";
import MenuCard from "@/components/home/MenuCard.vue";
import { products } from "./../database/menu.js";
</script>

<template>
  <section class="card_container">
    <MenuCard
      v-for="product in products"
      :key="product.name"
      :product="product"
    />
  </section>
</template>

<style scoped>
.card_container {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  gap: 20px;
  flex-wrap: wrap;
}
</style>
