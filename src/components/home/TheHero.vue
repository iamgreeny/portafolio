<script setup></script>

<template>
  <section>
    <img src="/images/hero.jpg" alt="" />
    <div class="hero-text">
      <h1>Pintando mis pensamientos</h1>
      <p>
        ¡Conoce a Meteora, la hechicera de los Colores! En su camino va
        transformando colores en historias visuales. El viaje creativo de
        Meteora es una aventura emocionante, siempre descubriendo nuevos
        tesoros. Ella explora el mundo de la imaginación sin miedo. Con sus
        ideas coloridas, quiere hacer del mundo un un poco más vibrante y
        encantador.
      </p>
    </div>
  </section>
</template>

<style scoped>
section {
  height: 500px;
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.hero-text {
  position: absolute;
  width: 40%;
  left: 100px;
  bottom: 100px;
}
</style>
