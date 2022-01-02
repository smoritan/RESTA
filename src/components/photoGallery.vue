<template>
  <div class="imageContainer">
    <transition-group name="fade" tag="div">
      <div v-for="i in [currentIndex]" :key="i">
        <img class="galleryIMG" :src="currentImg" />
      </div>
    </transition-group>
    <div class="imgTag">
      <h3>{{ currentTlt }}</h3>
    </div>
    <div class="shadow"><p class="ghostContent">..</p></div>
    <div class="textContainer">
      <h2 class="innerText"> Su sueño, Nuestro orgullo. </h2>
      <p class="innerText">Participamos en los sueños de muchos, apoyando el proceso y participando en el crecimiento de la cuidad y del país. Ver a nuestros clientes cumplir sus sueños es uno de los motores que impulsan el crecimiento de RESTA.</p>
    </div>
  </div>
</template>

<script>
import movistarArena from "../assets/movistarArenas.jpeg";
import donnaAqua from "../assets/donnaAqua.jpeg";
import aeroEzeiza from "../assets/AeroEzeiza.jpeg"

export default {

  name: 'PhotoGallery',
  data() {
    return {
      images: [
        movistarArena,
        donnaAqua,
        aeroEzeiza
      ],
      titles: [
        'Movistar Arena',
        'Edificio DONNA Aqua',
        'Aeropuerto Int. Ministro Pistarini'
      ],
      timer: null,
      currentIndex: 0
    };
  },

  mounted() {
    this.startSlide();
  },

  methods: {
    startSlide() {
      this.timer = setInterval(this.next, 6000);
    },

    next() {
      this.currentIndex += 1;
    },
    prev() {
      this.currentIndex -= 1;
    },
  },

  computed: {
    currentImg() {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
    },
    currentTlt() {
      return this.titles[Math.abs(this.currentIndex) % this.titles.length];
    }
  }
}
</script>

<style scoped>
@import "../styleComponents/photoGallery.scss";
</style>
