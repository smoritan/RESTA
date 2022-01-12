<template>
    <section id="us">
      <h1>Asi Somos.</h1>
      <div class="container">
        <div class="floted up">
          <img :src="picture2" class="floatImages"/>
        </div>
        <div class="floted fText down">
          <p>RESTA es una empresa líder, con más de 40 años de trayectoria en el mercado y un legado innegable.
              En 1978 Domingo Resta, nacido en Italia, comenzaba su sueño de progreso para él y los suyos.
              Décadas más tarde, su familia junto a un gran equipo,  mantienen vigente aquel legado. RESTA es sinónimo de confianza y servicio.
          </p>
        </div>
      </div>
      <div class="container">
        <div class="floted fText up">
          <p>RESTA comercializa productos de marcas líderes. Trabajamos con Empresas Constructoras, Instaladores, Estudios de Arquitectura y público en general, contamos con amplia flota de vehículos propios que hacen envíos a todo el país.
            Ofrecemos soluciones integrales en cada etapa de obra.
          </p>
        </div>
        <div class="floted down">
          <img :src="picture1" class="floatImages"/>
        </div>
      </div>
    </section>
</template>

<script>
import picture1 from "../assets/_DSC5166.jpg";
import picture2 from "../assets/_DSC2057.jpg";

export default {
  name: 'FloatBoxes',
  data() {
    return {
      picture1,
      picture2
    };
  },
}
</script>

<style scoped>
@import "../styleComponents/floatBoxes.scss";
</style>
