<script setup>
import SingleProject from "./SingleProject.vue";
</script>

<template>
  <section class="project">
    <img class="below_banner" src="/images/home/below_banner7.svg" alt="" />
    <div class="ph_container">
      <div class="text_block">
        <p>Inspired</p>
        <h1>Collection Portfolio</h1>
      </div>
      <div class="highlight_container">
        <SingleProject :projectIndex="0" />
        <SingleProject :projectIndex="7" />
        <SingleProject :projectIndex="3" />
      </div>
      <div class="dream"><img src="/images/home/fantasy.svg" alt="" /></div>
      <img class="durmiente" src="/images/home/nina_dream.svg" alt="" />
      <img class="ondascolores" src="/images/home/ondas_bajas.svg" alt="" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.ph_container {
  padding-top: 25rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.below_banner {
  position: absolute;
  width: 100%;
}
.text_block {
  display: flex;
  align-items: center;
  flex-direction: column;
  font-family: gilroy_regular;
  color: var(--color-primary);
  text-transform: uppercase;
  text-align: center;

  p {
    font-size: 1.9rem;
  }

  h1 {
    font-size: 2.5rem;
  }
}
.highlight_container {
  width: 78%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  margin-top: 2rem;
  gap: 2rem;
}

.dream {
  width: 80%;
  z-index: -1;
}

.durmiente {
  width: 80%;
  margin-top: 1%;
}

.ondascolores {
  position: absolute;
  bottom: 0%;
}

@media screen and (min-width: 1200px) {
  .ph_container {
    padding-top: 28rem;
  }
}

@media screen and (max-width: 1000px) {
  .ph_container {
    padding-top: 15rem;
  }

  .highlight_container {
    grid-template-columns: repeat(1, 1fr);
  }

  .dream {
    width: 180%;
  }
}

@media screen and (max-width: 600px) {
  .ph_container {
    padding-top: 15rem;
  }
}

@media screen and (max-width: 450px) {
  .ph_container {
    padding-top: 10rem;
  }
}
</style>
