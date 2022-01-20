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
                <a href="mailto:info@sanitariosresta.com.ar?"><button class="sendBTN">ENVIAR</button></a>
            </div>
        </div>
        <h3>Sumate a nuestra familia</h3>
        <div class="socialBox">
            <a href="https://mercadolibre.com/"><img :src="mercadolibre" class="socialSVG" alt="MercadoLibre"></a>
            <a href="https://www.linkedin.com/"><img :src="linkedIn" class="socialSVG" alt="LinkedIn"></a>
            <a href="https://www.linkedin.com/" class="facebookLogo"><img :src="facebook" class="socialSVG" alt="Facebook"></a>
            <a href="https://www.whatsapp.com/"><img :src="whatsapp" class="socialSVG" alt="WhatsApp"></a>
            <a href="https://ar.pinterest.com/"><img :src="pinterest" class="socialSVG" alt="Pinterest"></a>
        </div>
        <div class="map-responsive">
        <iframe src="https://www.google.com/maps/d/embed?mid=1pd0dd2M2O3nHymwxAOMqf7eFjpuA3k3y&ehbc=2E312F" width="1100" height="700" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </div>
    </div>
</template>

<script>
import mercadolibre from '../assets/SVG/mercadolibre.svg';
import linkedIn from '../assets/SVG/linkedIn.svg';
import whatsapp from '../assets/SVG/whatsapp.svg';
import pinterest from '../assets/SVG/pinterest.svg';
import facebook from '../assets/SVG/FacebookLogo.svg';

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
      facebook,
      whatsapp,
      pinterest
    };
  }
}
</script>


<style scoped>
@import "../styleComponents/contactSection.scss";
</style>