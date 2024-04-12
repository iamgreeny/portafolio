<script setup></script>

<template>
  <div class="footer">
    <h1>All content copyright Laura Verde 2024 ©</h1>
    <div class="redes">
      <img src="/images/contact/social1.svg" alt="" />
      <img src="/images/contact/social2.svg" alt="" />
      <img src="/images/contact/social3.svg" alt="" />
    </div>
  </div>
</template>

<style scoped>
.footer {
  background-color: #29235c;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.footer > h1 {
  font-family: gilroy_regular;
  text-transform: capitalize;
  font-weight: 100;
  text-align: center;
  color: white;
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
