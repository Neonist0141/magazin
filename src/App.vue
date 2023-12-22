<!-- src/App.vue -->

<template>
  <Header />
  <Katalog id="sectionKatalog"/>
  <Galereya id="sectionGalereya"/>
  <Kontakty id="sectionKontakty"/>
  <OKompanii id="sectionOKompanii"/>
  <Footer id="footer"/>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Katalog from './components/section/Katalog.vue';
import Galereya from './components/section/Galereya.vue';
import Kontakty from './components/section/Kontakty.vue';
import OKompanii from './components/section/OKompanii.vue';

export default {
  name: 'App',
  components: {
    Header,
    Katalog,
    Galereya,
    Kontakty,
    OKompanii,
    Footer
  }
};
</script>

<style>
  Header, Footer, #kontakty, #komentarii {
    border-radius: 5px;
    box-shadow: 0 0 5px dimgray;
    padding: 0.5cm 1cm;
  }

  Header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 5px;
    box-shadow: 0 0 5px dimgray;
    padding: 0.5cm 1cm;
    background-color: #3282b8;
    color: #bbe1fa;
  }

  Footer {
    background-color: #0f4c75;
    color: #bbe1fa;
  }

  #sectionKatalog {
    overflow-y: auto;
  }

  #sectionGalereya {
    display: none;
  }

  #sectionKontakty {
    padding: 5px;
    display: none;
    overflow-y: auto;
  }

  #sectionOKompanii {
    display: none;
    padding: 5px;
    overflow-y: auto;
  }
</style>
