<template>
    <section>
        <Tovar class="tovar" />
    </section>
</template>
  
<script>
import Tovar from '../Tovar.vue';
    export default {
        name: 'Katalog-section',
        components: {
            Tovar
        }
    };
</script>
  
<style scoped>
section {
    display: grid;
    grid-template: auto / repeat(5, 1fr);
    gap: 0.5cm;
}

section::-webkit-scrollbar {
    width: 5px;
}

section::-webkit-scrollbar-thumb {
    background-color: lightgray;
    border-radius: 10px;
}
</style>