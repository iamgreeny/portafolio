<script setup>
import { RouterLink, RouterView } from "vue-router";
import TheHeader from "@/components/layouts/TheHeader.vue";
import TheFooter from "@/components/layouts/TheFooter.vue";
</script>

<template>
  <TheHeader class="main-content" />
  <div class="main-content">
    <RouterView />
  </div>
  <TheFooter class="main-content" />
  <div class="intro-animation">
    <div id="meteor"></div>
  </div>
</template>

<style scoped>
#meteor {
  position: absolute;
  top: 50%;
  right: -100px; /* Adjust the value based on the meteor's width */
  transform: translate(0, -50%);
  width: 100px; /* Adjust the width of the meteor */
  height: 100px; /* Adjust the height of the meteor */
  background-color: yellow; /* Adjust the color of the meteor */
  border-radius: 50%;
  animation: meteorAnimation 2s forwards;
}

@keyframes meteorAnimation {
  0% {
    right: -100px; /* Adjust the initial position of the meteor */
  }
  50% {
    right: 50%; /* Adjust the halfway position of the meteor */
  }
  100% {
    right: 50%; /* Adjust the final position of the meteor */
  }
}
.intro-animation {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(207, 207, 255);
  z-index: -99;
  animation: fadeOut 1s 3s forwards;
}

@keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}

.main-content {
  opacity: 0;
  animation: fadeIn 1s 3s forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
