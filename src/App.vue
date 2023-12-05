<!-- src/App.vue -->

<template>
  <header>
      <article>
          <h1>Магазин рукодельных изделий</h1>
      </article>
      <Menu></Menu>
  </header>
</template>

<script>
import Menu from './components/Menu.vue';

export default {
  name: 'App',
  components: {
    Menu
  }
};
</script>

<style>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    grid-column: 1/3;
    border-radius: 5px;
    box-shadow: 0 0 5px dimgray;
    padding: 0.5cm 1cm;
  }
</style>
