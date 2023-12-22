<template>
    <section>
        <div class="conteyner">
            <div class="opisanie">
                <div class="imgOpisanie"></div>
                <p>"Сделай Сам" - это уникальное пространство, где каждый сможет найти именно то, что ему по душе. Мы специализируемся на продаже рукодельных изделий ручной работы, созданных талантливыми мастерами и мастерицами. В нашем ассортименте вы найдете множество уникальных товаров, которые будут радовать вас каждый день.</p>
            </div>
            <div class="osobennost osobennostiBlok">
                <p>Огромный выбор товаров ручной работы – от декоративных предметов интерьера до уютных аксессуаров.</p>
                <div class="imgOsobennosti" id="imgOsobennost1"></div>
            </div>
            <div class="osobennost2 osobennostiBlok">
                <div class="imgOsobennosti" id="imgOsobennost2"></div>
                <p>Возможность приобрести уникальные подарки для своих близких и друзей.</p>
            </div>
            <div class="osobennost3 osobennostiBlok">
                <p>Регулярное обновление ассортимента, чтобы у вас всегда был выбор свежих идей для вашего дома.</p>
                <div class="imgOsobennosti" id="imgOsobennost3"></div>
            </div>
            <div class="osobennost4 osobennostiBlok">
                <div class="imgOsobennosti" id="imgOsobennost4"></div>
                <p>Индивидуальный подход к каждому клиенту. Мы всегда рады помочь вам в выборе изделий, которые идеально подойдут для вашего интерьера или станут приятным сюрпризом для ваших близких.</p>
            </div>
            <div class="osobennost5 osobennostiBlok">
                <p>Мы верим, что рукоделие является одним из самых прекрасных способов самовыражения и проявления своей индивидуальности. Именно поэтому наша цель - собрать под одной крышей талантливых мастеров и предоставить им возможность поделиться своим творчеством с миром.</p>
                <div class="imgOsobennosti" id="imgOsobennost5"></div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'OKompanii-section'
}
</script>

<style scoped>
section::-webkit-scrollbar {
    width: 5px;
}

section::-webkit-scrollbar-thumb {
    background-color: lightgray;
    border-radius: 10px;
}
.conteyner {
    display: grid; 
    grid-template-columns: 0.1fr 1fr 0.1fr; 
    grid-template-rows: repeat(min-content, 6); 
    gap: 2px 0px; 
    grid-template-areas:
    ". opisanie opisanie"
    "osobennost osobennost ."
    ". osobennost2 osobennost2"
    "osobennost3 osobennost3 ."
    ". osobennost4 osobennost4"
    "osobennost5 osobennost5 ."; 
}

.opisanie {
    grid-area: opisanie;
    display: flex;
    align-items: center;
    gap: 20px;
}
.osobennost { grid-area: osobennost; justify-content: flex-end;}
.osobennost2 { grid-area: osobennost2; justify-content: flex-start;}
.osobennost3 { grid-area: osobennost3; justify-content: flex-end;}
.osobennost4 { grid-area: osobennost4; justify-content: flex-start;}
.osobennost5 { grid-area: osobennost5; justify-content: flex-end;}

.opisanie > p {
    font-size: 20pt;
}

.imgOpisanie {
    border-radius: 50%;
    height: 256px;
    aspect-ratio: 1/1;
    background-image: url(../../assets/rukodelie.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.osobennostiBlok {
    display: flex;
    align-items: center;
    gap: 20px;
}

.osobennostiBlok > p {
    font-size: 20pt;
}

.imgOsobennosti {
    height: 256px;
    aspect-ratio: 1/1;
    border-radius: 50%;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

#imgOsobennost1 {
    background-image: url(../../assets/rukodelnye_tovary.jpg);
}

#imgOsobennost2 {
    background-image: url(../../assets/rukodelnye_podarki.jpg);
}
#imgOsobennost3 {
    background-image: url(../../assets/rukodelnyy_asortiment.jpg);
}
#imgOsobennost4 {
    background-image: url(../../assets/obsluzhyvanie_klientov.jpg);
}
#imgOsobennost5 {
    background-image: url(../../assets/osobennost5.webp);
}
</style>