<template>
  <div class="bima-header-container">
    <div class="bima-header-content">
      <div class="header-left">
        <img src="@/assets/Header/img.png" alt="" @click="goToHome" />
      </div>
      <div class="header-right">
        <div class="right-top">
          <div class="top-center">
            <a href="#">Частным лицам</a>
            <a href="#">Корпоративным клиентам</a>
            <a href="#">Партнерам / Переход в ТИАС</a>
          </div>
          <div class="top-right">
            <div class="right-phone">
              <img src="@/assets/Header/Vector.png" alt="" />
              <p>(44) 601 55 11</p>
            </div>
            <div class="right-lang">
              <div class="lang-visible" @click="langActive">
                <span>{{ defaultLang.lang }}</span>
                <svg
                  width="9"
                  height="7"
                  viewBox="0 0 9 7"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  :class="isLangActive ? 'svg-active' : 'svg-deactive'"
                >
                  <path
                    d="M4.85118 6.00015L8.85622 1.99504C8.94893 1.90241 9 1.77875 9 1.6469C9 1.51504 8.94893 1.39139 8.85622 1.29875L8.56135 1.0038C8.3692 0.811878 8.05691 0.811878 7.86506 1.0038L4.50187 4.367L1.13495 1.00007C1.04224 0.907438 0.918654 0.856292 0.786876 0.856292C0.654949 0.856292 0.531365 0.907438 0.438585 1.00007L0.143784 1.29502C0.0510769 1.38773 3.78607e-06 1.51131 3.7803e-06 1.64316C3.77454e-06 1.77502 0.0510768 1.89867 0.143784 1.99131L4.15248 6.00015C4.24548 6.09301 4.36965 6.14401 4.50165 6.14371C4.63416 6.14401 4.75826 6.09301 4.85118 6.00015Z"
                    fill="currentcolor"
                  />
                </svg>
              </div>
              <div
                class="lang-hidden"
                :class="isLangActive ? 'active' : 'deactive'"
              >
                <div
                  class="lang-items"
                  v-for="(item, idx) in languages"
                  :key="idx"
                >
                  <span @click="selectLang(item)">{{ item.lang }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="right-bottom">
          <div class="bottom-center">
            <ul>
              <li>
                <div class="about-visible" @click="aboutActive">
                  <span>О нас</span>
                  <svg
                    width="9"
                    height="7"
                    viewBox="0 0 9 7"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                    :class="isAboutActive ? 'svg-active' : 'svg-deactive'"
                  >
                    <path
                      d="M4.85118 6.00015L8.85622 1.99504C8.94893 1.90241 9 1.77875 9 1.6469C9 1.51504 8.94893 1.39139 8.85622 1.29875L8.56135 1.0038C8.3692 0.811878 8.05691 0.811878 7.86506 1.0038L4.50187 4.367L1.13495 1.00007C1.04224 0.907438 0.918654 0.856292 0.786876 0.856292C0.654949 0.856292 0.531365 0.907438 0.438585 1.00007L0.143784 1.29502C0.0510769 1.38773 3.78607e-06 1.51131 3.7803e-06 1.64316C3.77454e-06 1.77502 0.0510768 1.89867 0.143784 1.99131L4.15248 6.00015C4.24548 6.09301 4.36965 6.14401 4.50165 6.14371C4.63416 6.14401 4.75826 6.09301 4.85118 6.00015Z"
                      fill="currentcolor"
                    />
                  </svg>
                </div>
                <div class="about-hidden" :class="isAboutActive ? 'about-active' : 'about-deactive'">
                    <a href="/our-group">Наша команда</a>
                    <a href="/contacts">Обратная связь</a>
                </div>
              </li>
              <li><a href="/">Главная</a></li>
              <li><a href="/news">Новости</a></li>
              <li>
                <div class="insurance-visible" @click="insuranceActive">
                    <span>Страховые услуги</span>
                    <svg
                    width="9"
                    height="7"
                    viewBox="0 0 9 7"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                    :class="isInsuranceActive ? 'svg-active' : 'svg-deactive'"
                  >
                    <path
                      d="M4.85118 6.00015L8.85622 1.99504C8.94893 1.90241 9 1.77875 9 1.6469C9 1.51504 8.94893 1.39139 8.85622 1.29875L8.56135 1.0038C8.3692 0.811878 8.05691 0.811878 7.86506 1.0038L4.50187 4.367L1.13495 1.00007C1.04224 0.907438 0.918654 0.856292 0.786876 0.856292C0.654949 0.856292 0.531365 0.907438 0.438585 1.00007L0.143784 1.29502C0.0510769 1.38773 3.78607e-06 1.51131 3.7803e-06 1.64316C3.77454e-06 1.77502 0.0510768 1.89867 0.143784 1.99131L4.15248 6.00015C4.24548 6.09301 4.36965 6.14401 4.50165 6.14371C4.63416 6.14401 4.75826 6.09301 4.85118 6.00015Z"
                      fill="currentcolor"
                    />
                  </svg>
                </div>

                <div class="insurance-hidden" :class="isInsuranceActive ? 'insurance-active' : 'insurance-deactive'">
                    <a href="/driving-insurance">Спокойствие за рулем</a>
                </div>
              </li>
              <li><a href="">Точки продаж</a></li>
            </ul>
          </div>
          <div class="bottom-right">
            <input type="text">
            <img src="@/assets/Header/Vector2.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "bima-header",
  data() {
    return {
      languages: [
        {
          id: 1,
          lang: "Uz",
        },
        {
          id: 2,
          lang: "En",
        },
        {
          id: 3,
          lang: "Ru",
        },
      ],
      defaultLang: { id: 1, lang: "Uz" },
      isLangActive: false,
      isAboutActive: false,
      isInsuranceActive: false
    };
  },
  methods: {
    goToHome(){
      this.$router.push('/')
    },
    langActive() {
      this.isLangActive = !this.isLangActive;
    },
    selectLang(e) {
      this.defaultLang = e;
    },
    aboutActive(){
        this.isAboutActive = !this.isAboutActive
    },
    insuranceActive(){
        this.isInsuranceActive = !this.isInsuranceActive
    }
  },
};
</script>
