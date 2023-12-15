<template>
    <div v-for="item in menuItems" :key="item.id">
        <div class="img" :style="{ backgroundImage: 'url(' + item.imageUrl + ')' }"></div>
        <p class="nazvanie">{{ item.nazvanie }}</p>
        <div class="btnKorsina">
          <p class="tsena">{{ item.tsena }} ₽</p>
          <button :id="'btn' + item.id" @click="KupitiTovar(item.id)">Купить</button>
        </div>
    </div>
</template>

<script>    

export default {
  name: 'Tovar-component',
  data() {
    return {
      menuItems: [
        { id: 1, imageUrl: require("../assets/tovar/kartina_maki.jpg"), nazvanie: 'Картина "Маки"', tsena: 7000},
        { id: 2, imageUrl: require("../assets/tovar/bolozhka_polevie_tsveti.jpg"), nazvanie: 'Обложка "Полевые цветы"', tsena: 2400,},
        { id: 3,  imageUrl: require("../assets/tovar/kartina_yuzhnaya_osen.jpg"), nazvanie: 'Картина маслом "Южная осень"', tsena: 10200,},
        { id: 4, imageUrl: require("../assets/tovar/kartina_maki.jpg"), nazvanie: 'Картина "Маки"', tsena: 7000},
        { id: 5, imageUrl: require("../assets/tovar/bolozhka_polevie_tsveti.jpg"), nazvanie: 'Обложка "Полевые цветы"', tsena: 2400,},
        { id: 6,  imageUrl: require("../assets/tovar/kartina_yuzhnaya_osen.jpg"), nazvanie: 'Картина маслом "Южная осень"', tsena: 10200,},
        { id: 7, imageUrl: require("../assets/tovar/kartina_maki.jpg"), nazvanie: 'Картина "Маки"', tsena: 7000},
        { id: 8, imageUrl: require("../assets/tovar/bolozhka_polevie_tsveti.jpg"), nazvanie: 'Обложка "Полевые цветы"', tsena: 2400,},
        { id: 9,  imageUrl: require("../assets/tovar/kartina_yuzhnaya_osen.jpg"), nazvanie: 'Картина маслом "Южная осень"', tsena: 10200,},
        { id: 10, imageUrl: require("../assets/tovar/kartina_maki.jpg"), nazvanie: 'Картина "Маки"', tsena: 7000},
        { id: 11, imageUrl: require("../assets/tovar/bolozhka_polevie_tsveti.jpg"), nazvanie: 'Обложка "Полевые цветы"', tsena: 2400,},
        { id: 12,  imageUrl: require("../assets/tovar/kartina_yuzhnaya_osen.jpg"), nazvanie: 'Картина маслом "Южная осень"', tsena: 10200,}
      ],
    };
  },
  methods: {
    KupitiTovar(id) {
      const btn = document.getElementById('btn'+id);
      btn.textContent = "Товар в корзине";
      btn.disabled = true;   
      btn.style.opacity = '0.5'   
    }
  }
};
</script>

<style scoped>
div {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: #bbe1fa;
  border-radius: 10px;
  border: 1px solid #bbe1fa;
}
p {
    color: #1b262c;
    margin-left: 0.5cm;
}
.tsena {
    font-size: 20pt;
    font-weight: bold;
}
.img {
    width: 100%;
    aspect-ratio: 1/1;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    margin-bottom: 0.5cm;
}

.btnKorsina {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin: 0 0.5cm 0.5cm 0;
}

button {
  width: fit-content;
  background-color: #3282b8;
  color: #bbe1fa;
  border: none;
  border-radius: 100px;
  padding: 5px 15px;
}

button:hover {
  cursor: pointer;
}
</style>