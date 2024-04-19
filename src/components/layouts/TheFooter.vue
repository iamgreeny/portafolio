<script setup>
import SocialLinks from "@/components/layouts/SocialLinks.vue";
</script>

<template>
  <div class="footer">
    <h1>All content copyright Laura Verde 2024 ©</h1>
    <SocialLinks />
  </div>
</template>

<style scoped>
.footer {
  background-color: #29235c;
  height: 150px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column-reverse;
  gap: 1rem;
}

.footer > h1 {
  font-family: gilroy_regular;
  text-transform: capitalize;
  font-weight: 100;
  text-align: center;
  color: #ffbd59;
  font-size: 1.2rem !important;
}

@media (max-width: 600px) {
  .footer > h1 {
    font-size: 14px;
  }
}

@media (min-width: 601px) and (max-width: 900px) {
  .footer > h1 {
    font-size: 18px;
  }
}

@media (min-width: 901px) {
  .footer > h1 {
    font-size: 24px;
  }
}
</style>
