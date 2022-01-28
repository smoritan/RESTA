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
                <a href="mailto:info@sanitariosresta.com.ar"><button class="sendBTN">ENVIAR</button></a>
            </div>
        </div>
        <h3>Sumate a nuestra familia</h3>
        <div class="socialBox">
            <a href="https://restasanitarios.mercadoshops.com.ar/"><img :src="mercadolibre" class="socialSVG" alt="MercadoLibre"></a>
            <a href="https://www.linkedin.com/company/restasanitarios"><img :src="linkedIn" class="socialSVG" alt="LinkedIn"></a>
            <a href="https://m.facebook.com/restaoficial" class="facebookLogo"><img :src="facebook" class="socialSVG" alt="Facebook"></a>
            <a href="https://api.whatsapp.com/send?phone=541131930074&text=%C2%A1Hola%21+Estoy+en+la+tienda+RESTA+y+quiero+pedir+m%C3%A1s+informaci%C3%B3n."><img :src="whatsapp" class="socialSVG" alt="WhatsApp"></a>
            <a href="https://pin.it/5VCEp0Y"><img :src="pinterest" class="socialSVG" alt="Pinterest"></a>
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
    // name: {
    //     type: String,
    //     default: ''
    // },
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
      pinterest,
      name: '',
    };
},
    computed: {
        console() {
            return console.log(this.data.name);
        }
    }
}
</script>


<style scoped>
@import "../styleComponents/contactSection.scss";
</style>