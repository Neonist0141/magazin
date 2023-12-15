<template>
    <section>
      <div class="wrapper">
        <div class="block" v-for="item in Items" :key="item.id" :id="'slide' + item.id">
          <a :href="'#slide' + Number(item.id-1)"><img class="arrow" src="../../assets/arrow-left.svg"></a>
          <img class="kartinka" :src="item.imageUrl">
          <a :href="'#slide' + Number(item.id+1)"><img class="arrow" src="../../assets/arrow-right.svg"></a>
        </div>
      </div>
    </section>
</template>

<script>
export default {
    name: "Galereya-section",
    data() {
    return {
      Items: [
        {id: 1, imageUrl: require("../../assets/tovar/kartina_maki.jpg")},
        {id: 2, imageUrl: require("../../assets/tovar/bolozhka_polevie_tsveti.jpg")},
        {id: 3, imageUrl: require("../../assets/tovar/kartina_yuzhnaya_osen.jpg")},
      ],
    };
    }
}
</script>

<style scoped>
section {
  display: grid;
  overflow: hidden;
  scroll-behavior: smooth;
}

section::-webkit-scrollbar {
  visibility: hidden;
}
.wrapper {
  display: flex;
  height: 100%;
}
.block {
  flex: 0 0 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

a {
  background-color: #3282b8;
  border-radius: 150px;
  display: flex;
  align-items: center;
  padding: 0.5cm;
  opacity: 0.5;
}

.kartinka {
  height: 100%;
}
</style>