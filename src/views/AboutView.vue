<script setup></script>

<template>
  <section class="content_container">
    <img id="onda" src="/images/about/ondas_superiores.svg" alt="" />
    <img id="flor" src="/images/about/flor_morada.svg" alt="" />

    <img class="photo" src="/images/about/p2.png" alt="" />

    <div class="text_about hide_mobile">
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
    <img id="plantas" src="/images/about/plantas_bajas.svg" alt="" />
  </section>
  <section class="text_section show_mobile">
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
  </section>
</template>

<style lang="scss" scoped>
.content_container {
  padding-top: 130%;
  overflow: hidden;
}

.hide_mobile {
  display: block;
}

.show_mobile {
  display: none;
}

h1 {
  text-wrap: nowrap;
}

.content_container > * {
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
  top: 27%;
  width: 31%;
  left: 50%;
  transform: translateX(-50%);
}

.text_about {
  text-align: center;
  top: 53%;
  width: 72%;
  left: 50%;
  transform: translateX(-50%);

  h1 {
    font-size: 5rem;
    font-family: morvem_font;
  }

  p {
    font-family: gilroy_regular;
  }
}

.avion {
  top: 71%;
  width: 51%;
  left: 51%;
  transform: translateX(-50%);
}

@media screen and (min-width: 1400px) {
  .text_about {
    h1 {
      font-size: 6rem;
    }
    p {
      font-size: 2rem;
    }
  }
}

@media screen and (min-width: 1200px) {
  .text_about {
    h1 {
      font-size: 6rem;
    }
    p {
      font-size: 1.5rem;
    }
  }
}

@media screen and (max-width: 900px) {
  .text_section {
    background: linear-gradient(90deg, #00a19a, #2fac66);
    padding-bottom: 40px;
  }

  .photo {
    top: 28%;
    width: 55%;
  }

  .text_about {
    top: 0%;
    width: 72%;

    h1 {
      font-size: 3rem;
      font-family: morvem_font;
    }

    p {
      font-size: 1.2rem;
      font-family: gilroy_regular;
    }
  }

  .hide_mobile {
    display: none;
  }
  .show_mobile {
    display: block;
  }
}

@media screen and (max-width: 600px) {
  .text_about {
    h1 {
    }

    p {
      font-size: 0.8rem;
    }
  }
}
</style>
