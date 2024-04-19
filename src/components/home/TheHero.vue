<script setup></script>

<template>
  <section>
    <img src="/images/home/banner10.svg" alt="" />
    <div class="hero-text">
      <h1>
        PAINTING MY <br />
        THOUGHTS
      </h1>
    </div>
  </section>
</template>

<style scoped>
section {
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
  display: block;
}

.hero-text {
  position: absolute;
  width: 40%;
  left: 5%;
  bottom: 17%;
}

h1 {
  font-family: gilroy_regular;
  color: #ffbd59;
  font-size: 2.2rem;
}

@media screen and (width > 1200px) {
  h1 {
    font-size: 4rem;
  }
}

@media screen and (width < 600px) {
  h1 {
    font-size: 1.4rem;
  }
}

@media screen and (width < 400px) {
  h1 {
    font-size: 1rem;
  }
}
</style>
