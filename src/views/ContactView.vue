<script setup>
import SocialLinks from "@/components/layouts/SocialLinks.vue";
</script>

<template>
  <section class="cont_papa">
    <h1>¡BIENVENIDO A MI MUNDO DE COLORES!</h1>
    <div class="form_cont">
      <div class="outer"><div class="inner"></div></div>
      <div class="outer"><div class="inner"></div></div>
      <div class="outer"><div class="inner"></div></div>
    </div>
    <SocialLinks />
    <img src="/images/contact/tortuga.svg" alt="" />
    <!-- aqui va la imagen nubestortuga-->
  </section>
</template>

<style scoped>
.cont_papa {
  display: flex;
  align-items: center;
  flex-direction: column;
}
h1 {
  display: flex;
  justify-content: center;
  margin-top: 7%;
  font-family: morvem_font;
  color: var(--color-primary);
  text-transform: uppercase;
  font-weight: 100;
  text-align: center;
  font-size: 6rem;
}
.form_cont {
  display: flex;
  flex-direction: column;
  width: 50%;
  border: 1px solid red;
  gap: 20px;
  margin-top: 4%;
}

.outer {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #efefef;
  height: 100px;
  border-radius: 40px;
  box-shadow: 5px 5px black;
}

.inner {
  background-color: #e27fa6;
  height: 80px;
  width: 95%;
  border-radius: 15px;
}
</style>
