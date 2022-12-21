<template>
  <div class="bima-news-container">
    <div class="bima-news-content">
      <div class="news-top">
        <h1>Новости</h1>
        <a href="/news">Все новости</a>
      </div>
      <div class="news-bottom">
        <div
          class="right-items"
          v-for="(item, idx) in news"
          :key="idx"
          :id="idx + 1"
          :class="{'active': idx+1 == 1}"
        >
        <img :src="require('@/assets/Content/ThreeNews/' + item.img)" alt="">
          <span>{{ item.date }}</span>
          <a href="#">{{ item.title }}</a>
          <p>{{ item.descript }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "news-content",
  data() {
    return {
      news: [
        {
          id: 1,
          img: "img1.png",
          date: "02.05.2021",
          title:
            "Первая международная олимпиада по ментальной арифметике «ШОСkids»",
          descript:
            "В Душанбе в Президентском лицее для одаренных детей состоялась Первая Международная Олимпиада по ментальной...",
        },
        {
          id: 2,
          img: "img2.png",
          date: "14.04.2021",
          title: "Самые яркие моменты к 7-летию страховой организации «BIMA»",
          descript:
            "Свой день рождения «BIMA» традиционно отмечает 14 апреля – дня получения первой лицензии на право ведения страховой...",
        },
        {
          id: 3,
          img: "img3.png",
          date: "30.01.2021",
          title:
            "Презентация новых страховых опций «Мобихранитель» и «Мобихранитель + »",
          descript:
            "В торговом центре Душанбе Мол (Ашан) состоялась презентация новых страховых опций «МобиХранитель» и «МобиХранитель...",
        },
        {
          id: 4,
          img: "img4.png",
          date: "09.01.2021",
          title:
            "Tcell и «BIMA» представляют опции для страхования мобильной техники",
          descript:
            "Ведущий инновационный оператор страны – компания Tcell и страховая компания BIMA Insurance представляют страховые опции...",
        },
        {
          id: 5,
          img: "img5.png",
          data: "17.05.2021",
          title:
            "Страховая организация «BIMA» отметила заслуги сотрудников банка «Арванд»",
          descript:
            "По завершении церемонии руководство Страховой организации «BIMA» выразила искреннюю благодарность всему коллективу...",
        },
      ],
    };
  },
};
</script>
