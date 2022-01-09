<template>
    <section id="us">
      <h1>Honrados de compartirle nuestra esencia.</h1>
      <div class="container">
        <div class="floted up">
          <img :src="picture1" class="floatImages"/>
        </div>
        <div class="floted fText down">
          <h2>Sed ut perspiciatis unde omnis iste natus error sit</h2>
          <p>RESTA es una empresa líder, con más de 40 años de trayectoria en el mercado y un legado innegable.
              En 1978 Domingo Resta, inmigrante italiano, comenzaba su sueño de progreso para él y los suyos, trabajando pesadas piezas de hierro fundido en el patio de una vieja casona en Floresta. 
              Décadas más tarde, su familia junto a un gran equipo,  mantienen vigente aquel legado: RESTA es sinónimo de confianza y servicio
              Nuestra moderna e innovadora Casa Central es reflejo de excelencia e inspiración. Contamos con más de 3000 mts 2.ubicados en pleno corazón de Buenos Aires.
          </p>
        </div>
      </div>
      <div class="container">
        <div class="floted fText up">
          <h2>Sed ut perspiciatis unde omnis iste natus error sit</h2>
          <p>RESTA comercializa productos de marcas líderes en los rubros: sanitarios, gas, incendio, calefacción, piscina, riego y herramientas. Además de loza, grifería, y accesorios, contamos con una amplia variedad en equipamiento para el hogar.
            Nuestros asesores ofrecen soluciones integrales brindando asesoramiento técnico y acompañando al cliente en cada etapa de obra.
            Trabajamos con  Empresas Constructoras, Instaladores, Estudios de Arquitectura y público en general,
            Contamos con amplia flota de vehículos propios que hacen envíos a todo el país.
          </p>
        </div>
        <div class="floted down">
          <img :src="picture2" class="floatImages"/>
        </div>
      </div>
    </section>
</template>

<script>
import picture1 from "../assets/_DSC5166.jpg";
import picture2 from "../assets/_DSC5129.jpg";

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
