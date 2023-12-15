<template>
    <header>
      <article>
            <img src="../assets/logo.svg" alt="Логотип">
            <p>
                Магазин рукодельных изделий<br>
                <span class="nazvanieSayta">"Сделай сам"</span>
            </p>
      </article>
      <Menu></Menu>
  </header>
</template>

<script>
import Menu from '../components/Menu.vue';

export default {
  name: 'Header-component',
  components: {
    Menu
  }
};
</script>

<style>
    article {
        display: flex;
        align-items: center;
        gap: 0.5cm;
    }
    img {
        height: 64px;
    }
    .nazvanieSayta {
        font-size: 20pt;
    }
    article > p {
        font-size: 14pt;
    }
</style>