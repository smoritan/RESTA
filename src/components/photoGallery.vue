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
      <p class="innerText">Atraves de los sueños de nuestros clientes participamos del crecimiento y desarrollo a lo largo de todo el país.</p>
    </div>
  </div>
</template>

<script>
import movistarArena from "../assets/movistarArenas.jpeg";
import donnaAqua from "../assets/donnaAqua.jpeg";
import aeroEzeiza from "../assets/AeroEzeiza.jpeg";
import CCK from "../assets/CCK.jpeg"
import bañoPic from "../assets/bathpic.jpeg";
import kitchenPic from "../assets/kitchen.jpeg";

export default {

  name: 'PhotoGallery',
  data() {
    return {
      images: [
        movistarArena,
        donnaAqua,
        aeroEzeiza,
        CCK,
        bañoPic,
        kitchenPic
      ],
      titles: [
        'Movistar Arena',
        'Edificio DONNA Aqua',
        'Aeropuerto Int. Ministro Pistarini',
        'Centro Culturar Nestor Kirchner',
        'RESTA - Especialista en Baños',
        'RESTA - Especialista en Cocinas'
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
