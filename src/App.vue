<!-- src/App.vue -->

<template>
  <header>
      <article>
          <h1>Магазин рукодельных изделий</h1>
      </article>
      <Menu></Menu>
  </header>
  <div>БЛОК</div>
  <div>БЛОК</div>
  <Footer></Footer>
</template>

<script>
import Menu from './components/Menu.vue';
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Menu,
    Footer
  }
};
</script>

<style>
  header, Footer {
    border-radius: 5px;
    box-shadow: 0 0 5px dimgray;
    padding: 0.5cm 1cm;
}

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    grid-column: 1/3;
    border-radius: 5px;
    box-shadow: 0 0 5px dimgray;
    padding: 0.5cm 1cm;
    background-color: #3282b8;
    color: #bbe1fa;
  }
  Footer {
    grid-column: 1/3;
    background-color: #0f4c75;
    color: #bbe1fa;
  }
</style>
