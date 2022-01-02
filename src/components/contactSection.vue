<template>
    <div>
        <h2>Comunicate con el equipo de RESTA</h2>
        <div class="emailContainer">
            <div class="infoCont">
                <input class="inputBox" v-model="name" placeholder="Nombre y Apellido">
                <input class="inputBox" v-model="email" placeholder="resta@example.com">
            </div>
            <div class="messageCont">
                <input class="emailBox" v-model="message" placeholder="example">
                <button>ENVIAR</button>
            </div>
        </div>
        <h3>Sumate a nuestra familia</h3>
        <div class="socialBox">
            <a href="https://www.whatsapp.com/"><img :src="whatsapp" class="socialSVG" alt="WhatsApp"></a>
            <a href="https://mercadolibre.com/"><img :src="mercadolibre" class="socialSVG" alt="MercadoLibre"></a>
            <a href="https://www.linkedin.com/"><img :src="linkedIn" class="socialSVG" alt="LinkedIn"></a>
            <a href="https://ar.pinterest.com/"><img :src="pinterest" class="socialSVG" alt="Pinterest"></a>
        </div>
        <iframe
            width="600"
            height="450"
            style="border:0"
            loading="lazy"
            allowfullscreen
            src="https://www.google.com/maps/embed/v1/place?q=place_id:ChIJX8nW6OrJvJURsXgtm6dij-w&key=...">
        </iframe>
    </div>
</template>

<script>
import mercadolibre from '../assets/SVG/mercadolibre.svg';
import linkedIn from '../assets/SVG/linkedIn.svg';
import whatsapp from '../assets/SVG/whatsapp.svg';
import pinterest from '../assets/SVG/pinterest.svg';

export default {
props: {
    name: {
        type: String,
        default: ''
    },
    email: {
        type: String,
        default: ''
    },
    message: {
        type: String,
        default: ''
    }
},
data() {
    return {
      mercadolibre,
      linkedIn,
      whatsapp,
      pinterest
    };
  }
}
</script>


<style scoped>
@import "../styleComponents/contactSection.scss";
</style>