<template>
    <section>
            <article id="kontakty">
            <div id="divTelefon" class="blockKontakty">
                <img src="../../assets/phone-call.svg">
                <p>Телефон<br>
                    <span>{{ phone }}</span>
                </p>
            </div>
        <div id="divEmail" class="blockKontakty">
            <img src="../../assets/email.svg">
            <p>Электронная почта<br>
                    <span>{{ email }}</span>
            </p>
        </div>
        <div id="divOperator" class="blockKontakty">
            <img src="../../assets/call-support.svg">
            <p>Режим работы операторов<br>
                <span>{{ operator }}<br>{{ operator2 }}</span>
            </p>
        </div>
        <div id="divDostavka" class="blockKontakty">
            <img src="../../assets/deliver-truck.svg">
            <p>Режим работы службы доставки<br>
                    <span>{{ deliver }}</span>
            </p>
        </div>
        <div id="divAdres" class="blockKontakty">
            <img src="../../assets/info.svg">
            <p>Юридическая информация<br>
                    <span>ООО "Сделай сам"<br>{{ legalAddress }}</span>
                </p>
        </div>
        </article>
        <article id="komentarii">
            <h1>Коментарии</h1>
            <form @submit.prevent="addEntry" class="forma-zapis">
                <input type="text" class="input" v-model="newMessage">
                <button class="buttonKoment" :disabled="newMessage === ''">Добавить</button>
            </form>
            <div class="zapis-block">
                <div v-if="entries.length === 0">Оставте первый комментарий</div>
                <div v-else>
                    <span v-show="entries.length > 0">Всего {{ entryCount }} {{ pluralize }}</span>
                    <div class="zapis" v-for="(entry, index) in entries" :key="index" style="word-wrap: break-word;">
                        {{ entry.text }} - {{ new Intl.DateTimeFormat('ru', {year: "numeric", month: "numeric", day: "numeric", hour: "numeric", minute: "numeric"}).format(entry.date) }}
                    </div>
                </div>
            </div>
        </article>
    </section>
</template>

<script>
export default {
    name: 'Kontakty-section',
    data() {
    return {
        newMessage: '',
      entries: [],
      phone: '+7 (999) 515-74-50',
      email: 'SvetlovAantoliyS@yandex.ru',
      legalAddress: 'г. Гатчина',
      operator: 'Пн-Пт 08:00 до 22:00 по Москве',
      operator2: 'Сб-Вс 09:00 до 21:00 по Москве',
      deliver: 'Уточнять у выбранной службы доставки'
    }
    },
    computed: {
    entryCount() {
      return this.entries.length;
    },
    pluralize() {
      return this.entryCount === 1 ? 'запись' : 'записи';
    }
    },
    methods: {
    addEntry() {
      this.entries.push({
        text: this.newMessage,
        date: Date.now()
      });
      this.newMessage = '';
    }
  }
}
</script>

<style>
#kontakty {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}

.blockKontakty {
    display: flex;
    align-items: center;
    gap: 10px;
}
#kontakty img {
    height: 48px;
}
#kontakty span {
    font-size: 18pt;
    font-weight: bold;
    color: black;
}
#kontakty p {
    color: #3282b8;
}
#komentarii {
    margin-top: 0.5cm;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}
.forma-zapis {
    display: flex;
    gap: 0.25cm;
}
.buttonKoment {
    background-color: #3282b8;
    border-radius: 100px;
    border: none;
    color: #bbe1fa;
    padding: 5px 10px;
}
.buttonKoment:disabled {
    opacity: 0.5;
}
</style>