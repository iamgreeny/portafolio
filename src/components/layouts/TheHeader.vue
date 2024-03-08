<script setup>
import { useRouter } from "vue-router";

const router = useRouter();
const navigateTo = (path) => {
  router.push(path);
};
</script>

<template>
  <header>
    <div class="titulo">
      <h1 @click="navigateTo('/')">meteora</h1>
    </div>
    <div class="links">
      <p @click="navigateTo('/work')">WORK</p>
      <p @click="navigateTo('/about')">ABOUT</p>
      <p @click="navigateTo('/contact')">CONTACT</p>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 80px;
  display: flex;
  justify-content: space-between;
  padding: 0px 20px;
  align-items: center;
  border-bottom: 1px solid black;
}

.titulo {
  h1 {
    text-transform: capitalize;
    font-family: kaoly_font;
    cursor: pointer;
  }
}

.links {
  display: flex;
  flex-direction: row;
  gap: 20px;
  font-family: gilroy_regular;
  p {
    cursor: pointer;
    transition: 0.3s;
    &:hover {
      text-shadow: 0px 0px 1px black;
    }
  }
}
</style>
