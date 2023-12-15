<!-- Menu.vue -->

<template>
    <ul>
      <li v-for="item in menuItems" :key="item.id" @click="functionKakayato(item.text)">
        {{ item.text }}
      </li>
      <img src="../assets/basket.svg" @click="Message">
    </ul>
</template>

<script>
export default {
  name: 'Menu-component',
  data() {
    return {
      menuItems: [
        { id: 1, text: 'Каталог' },
        { id: 1, text: 'Галерея' },
        { id: 2, text: 'Контакты' },
        { id: 3, text: 'О нас' }
      ],
    };
  },
  methods: {
    functionKakayato(item) {
      switch (item) {
        case "Галерея":
          document.getElementById("sectionGalereya").style.display = "block";
          document.getElementById("sectionKatalog").style.display = "none";
          document.getElementById("sectionKontakty").style.display = null;
          break;
        case "Контакты":
          document.getElementById("sectionGalereya").style.display = null;
          document.getElementById("sectionKatalog").style.display = "none";
          document.getElementById("sectionKontakty").style.display = "block";
          break;
        case "Каталог":
          document.getElementById("sectionGalereya").style.display = null;
          document.getElementById("sectionKatalog").style.display = null;
          document.getElementById("sectionKontakty").style.display = null;
          break;
        
        default:
          break;
      }
    },
    Message() {
      alert('Корзина в данный момент недоступна')
    }
  }
};
</script>

<style scoped>
/* Стили, специфичные для этого компонента */
ul {
  list-style-type: none;
  display: flex;
  align-items: center;
  padding: 0;
  gap: 15px;
}

li {
  padding: 5px 15px; 
  cursor: pointer;
  background-color: #0f4c75;
  border-radius: 100px;
}

img {
  height: 48px;
}

img:hover {
  cursor: pointer;
}
</style>
