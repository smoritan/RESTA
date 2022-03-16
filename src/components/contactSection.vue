<template>
    <div>
        <h2>Comunicate con el equipo de RESTA</h2>
        <div class="emailContainer">
            <button class="contactBtn"> <a href="mailto:info@sanitariosresta.com.ar" >Envíanos tu consulta por mail</a> </button>
        </div>
        <h3>Sumate a nuestra familia</h3>
        <div class="socialBox">
            <a href="https://m.facebook.com/restaoficial" class="facebookLogo"><img :src="facebook" class="socialSVG" alt="Facebook"></a>
            <a href="https://www.linkedin.com/company/restasanitarios"><img :src="linkedIn" class="socialSVG" alt="LinkedIn"></a>
            <a href="https://www.instagram.com/restaoficial/" ><img :src="instagram" class="socialSVG" alt="Instragram"></a>
            <!-- <a href="https://api.whatsapp.com/send?phone=541131930074&text=%C2%A1Hola%21+Estoy+en+la+tienda+RESTA+y+quiero+pedir+m%C3%A1s+informaci%C3%B3n."><img :src="whatsapp" class="socialSVG" alt="WhatsApp"></a> -->
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
import instagram from '../assets/SVG/instagram-2-1.svg'

export default {
props: {
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
      instagram,
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