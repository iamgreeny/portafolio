<script setup>
import SingleProject from "./SingleProject.vue";
</script>

<template>
  <section>
    <img class="below_banner" src="/images/home/below_banner3.svg" alt="" />
    <div class="ph_container">
      <div class="text_block">
        <p>Inspirate</p>
        <h1>Portafolio de Colecciones</h1>
      </div>
      <div class="highlight_container">
        <SingleProject />
        <SingleProject />
        <SingleProject />
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
}
.below_banner {
  position: absolute;
  width: 100%;
  top: 0px;
}
.text_block {
  display: flex;
  align-items: center;
  flex-direction: column;
  font-family: gilroy_regular;
  color: var(--color-primary);
  text-transform: uppercase;
  font-weight: 900;
  text-align: center;

  p {
    font-size: 1.8rem;
  }

  h1 {
    font-size: 2.5rem;
  }
}
.highlight_container {
  width: 60%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  margin-top: 2rem;
  gap: 2rem;
}

.dream {
  width: 60%;
  top: -50px;
  z-index: -1;
}

.durmiente {
  width: 80%;
}

.ondascolores {
  position: absolute;
  bottom: 0%;
}

@media screen and (width > 1200px) {
  .ph_container {
    padding-top: 15rem;
  }
}

@media screen and (width < 1000px) {
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

@media screen and (width < 600px) {
  .ph_container {
    padding-top: 8rem;
  }
}
</style>
