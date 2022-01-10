<template>
  <div id="app">
    <section class="firstSection" :style="{ backgroundImage: `url(${firstSectionImage})` }">
      <div class="helper">
        <button class="helperbtn" @click="goto('nosotros')">Nosotros</button>
        <button class="helperbtn" @click="goto('clientes')">Clientes</button>
        <button class="helperbtn" @click="goto('proveedores')">Proveedores</button>
        <button class="helperbtn" @click="goto('contacto')">Contacto</button>
      </div>
      <h1 class="title">RESTA</h1>
    </section>
    <section id="us-section" ref="nosotros">
      <floatBoxes></floatBoxes>
      <div class="contAccess" :style="{ backgroundImage: `url(${contactAccess})` }">
        <button class="btnContact" @click="goto('contacto')">Contactanos</button>
      </div>
    </section>
    <section class="clients" ref="clientes">
      <photoGallery></photoGallery>
    </section>
    <section class="providers" ref="proveedores">
      <providerSection></providerSection>
    </section>
    <section class="contact" ref="contacto">
      <contactSection></contactSection>
    </section>
    <section class="footerSect">
      <footerSection></footerSection>
    </section>
  </div>
</template>

<script>
import firstSectionImage from "./assets/_DSC4925.jpg";
import contactAccess from './assets/contactAccessBG.png'
import floatBoxes from "./components/floatBoxes.vue";
import photoGallery from "./components/photoGallery.vue";
import providerSection from "./components/providerSection.vue";
import contactSection from "./components/contactSection.vue"
import footerSection from "./components/footer.vue"

export default {
  name: 'App',
  components: {
    floatBoxes,
    photoGallery,
    providerSection,
    contactSection,
    footerSection
  },
  data() {
    return {
      firstSectionImage,
      contactAccess,
    };
  },
  methods: {
     goto(refName) {
      const element = this.$refs[refName];
      const top = element.offsetTop;

      window.scrollTo(0, top);
    }
  }
}
</script>

<style>
@import "./style.scss";
@import "./styleComponents/floatBoxes.scss";

#app {
  font-family: DINNEXT, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #FFFFFF;
  margin: 0;
  scroll-behavior: smooth;
}
body {
  margin: 0;
}
.contAccess {
  background-size: cover;
  height: 192px;
  justify-content: center;
  display: flex;
}

.btnContact {background-image: linear-gradient(to right, #77A1D3 0%, #79CBCA  51%, #77A1D3  100%)}
.btnContact {
  font-size: 2em;
  font-weight: 600;
  border: none;
  margin: auto;
  padding: 15px 45px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: #e7e7e8;            
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
  display: block;
}

.btnContact:hover {
  background-position: right center; /* change the direction of the change here */
  color: #e7e7e8;
  text-decoration: none;
}

.contact {
  background-color: #58585a;
  padding: 2% 5% 5%;
}

@media only screen and (max-width : 1300px) {
  .btnContact {
    font-size: 1.5em;
    margin-top: 8%;
    margin-bottom: 8%;
  }
  .contAccess {
    background-position: center center;
    background-repeat: no-repeat;
    background-attachment: initial;
    background-size: cover;
    height: auto;
  }
}

@media only screen and (max-width : 600px) {
  .btnContact {
    font-size: 1em;
  }
}

.footerSect {
  background-color: #767679;
  padding: 2%;
}
</style>
