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
    <img id="meteor" src="/images/cometa/meteor.svg" alt="meteor image" />
    <div id="clouds">
      <div class="cloud-left">
        <img src="/images/cometa/clouds_left.svg" alt="clouds" />
      </div>
      <div class="cloud-mid">
        <img src="/images/cometa/clouds_mid.svg" alt="clouds" />
      </div>
      <div class="cloud-right">
        <img src="/images/cometa/clouds_right.svg" alt="clouds" />
      </div>
    </div>
  </div>
</template>

<style scoped>
#meteor {
  position: absolute;
  top: 40%;
  right: -500px; /* Adjusta el valor basado en el ancho del meteorito */
  transform: translate(60%, -50%);
  width: 500px; /* Ajusta el ancho del meteorito según lo necesites */
  height: auto; /* Permite que la altura se ajuste automáticamente para mantener la proporción */
  animation: meteorAnimation 3s forwards ease-out;
}

@keyframes meteorAnimation {
  0% {
    right: -500px; /* Adjust the initial position of the meteor */
    top: 40%;
  }
  50% {
    right: 50%; /* Adjust the halfway position of the meteor */
    top: 50%;
  }
  100% {
    right: 50%; /* Adjust the final position of the meteor */
    top: 50%;
  }
}
.intro-animation {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to top, #40006b, #6700ab);
  z-index: -99;
  animation: fadeOut 1s 3s forwards;
}

#clouds {
  display: flex;
  align-items: end;
  width: 100%;
  height: 100%;
  position: absolute;
}

.cloud-left {
  flex: 2;
}

.cloud-mid {
  flex: 1;
}

.cloud-right {
  flex: 2;
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

@media screen and (max-width: 600px) {
  .cloud-mid {
    display: none;
  }

  #meteor {
    width: 208px;
    height: auto;
  }

  .intro-animation {
    width: 100dvw;
    width: 100vw;
    height: 100dvh;
    height: 100vh;
  }
}
</style>
