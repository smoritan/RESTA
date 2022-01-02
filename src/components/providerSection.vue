<template>
    <div>
        <div class="infoContainer">
            <div class="ourProvider">
                <h2 class="titleDesc">Nuestros Proveedores</h2>
                <p class="textDesc">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</p>
            </div>
             <div class="fraseContainer">
                <span class="titleCont">
                    <img src="../assets/delivery-box.svg" class="svg">
                    <h2 class="titleFrase">Nuestros Proveedores</h2>
                    </span>
                <p class="frase">“Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel facilisis.” </p>
            </div>
        </div>
        <div class="carousel">
            <div class="inner">
                <div class="card" v-for="card in cards" :key="card">
                    <img :src="card">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import rec61 from '../assets/SVG/Recurso 61_.svg';
import rec62 from '../assets/SVG/Recurso 62_.svg';
import rec63 from '../assets/SVG/Recurso 63_.svg';
import rec64 from '../assets/SVG/Recurso 64_.svg';
import rec65 from '../assets/SVG/Recurso 65_.svg';
import rec66 from '../assets/SVG/Recurso 66_.svg';
import rec67 from '../assets/SVG/Recurso 67_.svg';
import rec68 from '../assets/SVG/Recurso 68_.svg';
import rec70 from '../assets/SVG/Recurso 70_.svg';
import rec71 from '../assets/SVG/Recurso 71_.svg';
import rec72 from '../assets/SVG/Recurso 72_.svg';
import rec73 from '../assets/SVG/Recurso 73_.svg';
import rec74 from '../assets/SVG/Recurso 74_.svg';
import rec75 from '../assets/SVG/Recurso 75_.svg';
import rec76 from '../assets/SVG/Recurso 76_.svg';
import rec77 from '../assets/SVG/Recurso 77_.svg';
import rec78 from '../assets/SVG/Recurso 78_.svg';
import rec79 from '../assets/SVG/Recurso 79_.svg';
import rec80 from '../assets/SVG/Recurso 80_.svg';
import rec81 from '../assets/SVG/Recurso 81_.svg';
import rec82 from '../assets/SVG/Recurso 82_.svg';
import rec83 from '../assets/SVG/Recurso 83_.svg';
import rec84 from '../assets/SVG/Recurso 84_.svg';
import rec85 from '../assets/SVG/Recurso 85_.svg';
import rec86 from '../assets/SVG/Recurso 86_.svg';

export default {
data () {
    return {
        cards: [rec61, rec62, rec63, rec64, rec65, rec66, rec67, rec68, rec70, rec71, rec72, rec73, rec74, rec75, rec76, rec77, rec78, rec79, rec80, rec81, rec82, rec83, rec84, rec85, rec86]
    }
},
components: {
  }
}
</script>


<style scoped>
@import "../styleComponents/providerSection.scss";
</style>