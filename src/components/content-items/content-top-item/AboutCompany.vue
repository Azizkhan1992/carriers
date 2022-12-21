<template>
  <div class="about-company-container">
    <div class="about-company-content">
      <div class="about-company-top">
        <h1>О компании в цифрах</h1>
        <div class="top-center">
          <img src="@/assets/Content/FiveAboutCompany/img1.png" alt="" />
          <p>Год основания: <i>2014</i></p>
        </div>
        <div class="top-right">
          <div class="years-visible" @click="yearsActive">
            <span>{{ yearActive }} год</span>
            <img
              src="@/assets/Content/FiveAboutCompany/Vector.png"
              alt=""
              :class="isYearsActive ? 'img-active' : 'img-deactive'"
            />
          </div>
          <div
            class="years-hidden"
            :class="isYearsActive ? 'years-active' : 'years-deactive'"
          >
            <div
              class="year-items"
              v-for="(year, idx) in years"
              :key="idx"
              @click="selectYear(year)"
            >
              <span>{{ year }} год</span>
            </div>
          </div>
        </div>
      </div>
      <div class="about-company-bottom">
        <div class="about-bottom-left">
          <div class="left-items">
            <img src="@/assets/Content/FiveAboutCompany/img1.svg" alt="" />
            <div class="item-title">
              <p>{{ selectedInsurance.humanIns }}</p>
              <span>человек застраховано</span>
            </div>
          </div>
          <div class="left-items">
            <img src="@/assets/Content/FiveAboutCompany/img2.svg" alt="" />
            <div class="item-title">
              <p>{{ selectedInsurance.avtoIns }}</p>
              <span>машин застраховано</span>
            </div>
          </div>
          <div class="left-items">
            <img src="@/assets/Content/FiveAboutCompany/img3.svg" alt="" />
            <div class="item-title">
              <p>{{ selectedInsurance.paidIns }}</p>
              <span>выплачено по страховым случаям</span>
            </div>
          </div>
          <div class="left-items">
            <img src="@/assets/Content/FiveAboutCompany/img4.svg" alt="" />
            <div class="item-title">
              <p>{{ selectedInsurance.gettingIns }}</p>
              <span>страховой премии получено</span>
            </div>
          </div>
          <div class="left-items">
            <img src="@/assets/Content/FiveAboutCompany/img5.svg" alt="" />
            <div class="item-title">
              <p>{{ selectedInsurance.turIns }}</p>
              <span>выезжающих за рубеж застраховано</span>
            </div>
          </div>
          <div class="left-items">
            <img src="@/assets/Content/FiveAboutCompany/img6.svg" alt="" />
            <div class="item-title">
              <p>{{ selectedInsurance.policyIns }}</p>
              <span>полисов выпущено</span>
            </div>
          </div>
        </div>
        <div class="about-bottom-right">
            <img src="@/assets/Content/FiveAboutCompany/Tajikistan1.svg" alt="">
            <img src="@/assets/Content/FiveAboutCompany/img7.svg" alt="" class="img-one">
            <p class="title-one">Худжанд</p>

            <img src="@/assets/Content/FiveAboutCompany/img7.svg" alt="" class="img-two">
            <p class="title-two">Душанбе</p>

            <img src="@/assets/Content/FiveAboutCompany/img7.svg" alt="" class="img-three">
            <p class="title-three">Бохтар</p>

            <img src="@/assets/Content/FiveAboutCompany/img7.svg" alt="" class="img-four">
            <p class="title-four">Хорог</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "about-company",
  data() {
    return {
      yearActive: new Date().getFullYear(),
      isYearsActive: false,
      insurance: [
        {
          val: 2022,
          humanIns: "32 619",
          paidIns: "7 462 500",
          turIns: "11 392",
          avtoIns: "743",
          gettingIns: "51 250 597",
          policyIns: "50 000",
        },
        {
          val: 2021,
          humanIns: "28 354",
          paidIns: "5 967 300",
          turIns: "8 950",
          avtoIns: "545",
          gettingIns: "42 346 558",
          policyIns: "32 000",
        },
        {
          val: 2020,
          humanIns: "22 452",
          paidIns: "3 565 200",
          turIns: "7 548",
          avtoIns: "354",
          gettingIns: "38 476 935",
          policyIns: "27 500",
        },
        {
          val: 2019,
          humanIns: "25 568",
          paidIns: "6 354 400",
          turIns: "10 265",
          avtoIns: "637",
          gettingIns: "47 658 650",
          policyIns: "38 000",
        },
        {
          val: 2018,
          humanIns: "20 645",
          paidIns: "5 654 940",
          turIns: "9 463",
          avtoIns: "562",
          gettingIns: "44 327 578",
          policyIns: "35 000",
        },
        {
          val: 2017,
          humanIns: "20 907",
          paidIns: "4 845 650",
          turIns: "9 257",
          avtoIns: "532",
          gettingIns: "41 563 287",
          policyIns: "32 000",
        },
        {
          val: 2016,
          humanIns: "17 548",
          paidIns: "4 242 548",
          turIns: "8 646",
          avtoIns: "437",
          gettingIns: "39 648",
          policyIns: "29 500",
        },
        {
          val: 2015,
          humanIns: "18 365",
          paidIns: "4 465 596",
          turIns: "8 845",
          avtoIns: "488",
          gettingIns: "41 455",
          policyIns: "30 400",
        },
        {
          val: 2014,
          humanIns: "16 755",
          paidIns: "4 846 688",
          turIns: "9 255",
          avtoIns: "536",
          gettingIns: "43 675",
          policyIns: "33 000",
        },
      ],
    };
  },
  computed: {
    selectedInsurance() {
      let activeInsurance;
      this.insurance.forEach((elem) => {
        if (elem.val == this.yearActive) {
          activeInsurance = elem;
        }
      });
      return activeInsurance;
    },
    years() {
      let years = [];
      let nowDate = new Date().getFullYear();
      for (let i = nowDate - 8; i < nowDate + 1; i++) {
        years.push(i);
      }
      return years;
    },
  },
  methods: {
    yearsActive() {
      this.isYearsActive = !this.isYearsActive;
    },
    selectYear(e) {
      this.yearActive = e;
    },
  },
};
</script>
