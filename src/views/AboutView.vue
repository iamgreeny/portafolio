<script setup></script>

<template>
  <section>
    <img id="onda" src="/images/about/ondas_superiores.svg" alt="" />
    <img id="flor" src="/images/about/flor_morada.svg" alt="" />
    <img id="plantas" src="/images/about/plantas_bajas.svg" alt="" />

    <img class="photo" src="/images/about/p2.png" alt="" />

    <div class="text_about">
      <h1>Hola! Soy Meteora</h1>
      <p>
        Me llaman la hechicera de los Colores! Soy una artista en diseño gráfico
        e ilustración con un toque mágico. Transformando colores en visuales
        historias y mensajes con un golpe social. Mi viaje creativo es una
        aventura emocionante, siempre descubriendo nuevos tesoros. Exploro el
        mundo de la imaginación y los sueños sin miedo. Con mis ideas coloridas,
        quiero hacer del mundo un poco más vibrante y encantador, con diseño e
        ilustración. Trabajo comunicando de manera visual composiciones
        artisticas que satisfagan sus necesidades.
      </p>
    </div>

    <img class="avion" src="/images/about/avion.svg" alt="" />
  </section>
</template>

<style lang="scss" scoped>
section {
  padding-top: 130%;
  overflow: hidden;
}

section > * {
  position: absolute;
}

#onda {
  top: 0px;
}

#flor {
  top: 13%;
}

#plantas {
  bottom: 0px;
}

.photo {
  top: 24%;
  width: 20%;
  left: 50%;
  transform: translateX(-50%);
}

.text_about {
  text-align: center;
  top: 44%;
  width: 60%;
  left: 50%;
  transform: translateX(-50%);

  p {
    font-family: adventuro_font;
  }
}

.avion {
  top: 54%;
  width: 20%;
  left: 50%;
  transform: translateX(-50%);
}
</style>
