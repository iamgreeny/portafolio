<script setup></script>

<template>
  <header>
    <div class="titulo">
      <h1>meteora</h1>
    </div>
    <div class="links">
      <p>WORK</p>
      <p>ABOUT</p>
      <p>CONTACT</p>
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
}

.titulo {
  h1 {
    text-transform: capitalize;
    font-family: kaoly_font;
  }
}

.links {
  display: flex;
  flex-direction: row;
  gap: 20px;
  font-family: gilroy_regular;
}
</style>
