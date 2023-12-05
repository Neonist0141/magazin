<!-- Menu.vue -->

<template>
    <ul>
      <li v-for="item in menuItems" :key="item.id">
        {{ item.text }}
      </li>
    </ul>
</template>

<script>
export default {
  name: 'Menu-component',
  data() {
    return {
      menuItems: [
        { id: 1, text: 'Каталог' },
        { id: 1, text: 'Аукцион' },
        { id: 2, text: 'Контакты' },
        { id: 3, text: 'О нас' }
      ]
    };
  }
};
</script>

<style scoped>
/* Стили, специфичные для этого компонента */
ul {
  list-style-type: none;
  display: flex;
  padding: 0;
  gap: 15px;
}

li {
  padding: 5px 15px; 
  cursor: pointer;
  background-color: #eee;
  border-radius: 100px;
}
</style>
