<template>
  <div class="bima-reviews-container">
    <div class="bima-reviews-content">
      <div class="reviews-top">
        <h1>Отзывы</h1>
        <div class="reviews-top-right">
          <button @click="moveLeft">
            <svg
              width="10"
              height="20"
              viewBox="0 0 10 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M0.503422 9.98627C0.502825 9.68083 0.609332 9.38483 0.804457 9.14964L7.34869 1.30623C7.57085 1.03927 7.8901 0.871386 8.23619 0.839516C8.58229 0.807646 8.92688 0.914397 9.19417 1.13629C9.46146 1.35817 9.62954 1.67702 9.66145 2.02269C9.69336 2.36836 9.58648 2.71253 9.36432 2.97949L3.50068 9.98627L9.1549 16.9931C9.26362 17.1268 9.34481 17.2806 9.39381 17.4458C9.4428 17.6109 9.45863 17.7841 9.44038 17.9554C9.42214 18.1267 9.37018 18.2927 9.2875 18.4439C9.20481 18.595 9.09303 18.7284 8.95858 18.8363C8.824 18.956 8.66612 19.0466 8.49482 19.1026C8.32353 19.1585 8.14251 19.1785 7.96312 19.1614C7.78372 19.1442 7.60982 19.0902 7.45229 19.0027C7.29476 18.9153 7.15701 18.7963 7.04766 18.6532L0.725926 10.8098C0.561645 10.5679 0.483304 10.2779 0.503422 9.98627Z"
                fill="currentcolor"
              />
            </svg>
          </button>
          <button @click="moveRight">
            <svg
              width="10"
              height="20"
              viewBox="0 0 10 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9.49658 9.98627C9.49718 9.68083 9.39067 9.38483 9.19554 9.14964L2.65131 1.30623C2.42915 1.03927 2.1099 0.871386 1.76381 0.839516C1.41771 0.807646 1.07312 0.914397 0.805831 1.13629C0.538543 1.35817 0.370456 1.67702 0.338546 2.02269C0.306637 2.36836 0.413519 2.71253 0.635681 2.97949L6.49932 9.98627L0.845098 16.9931C0.736377 17.1268 0.655187 17.2806 0.606195 17.4458C0.557202 17.6109 0.541373 17.7841 0.559617 17.9554C0.577862 18.1267 0.629819 18.2927 0.712504 18.4439C0.795189 18.595 0.906971 18.7284 1.04142 18.8363C1.176 18.956 1.33388 19.0466 1.50518 19.1026C1.67647 19.1585 1.85749 19.1785 2.03688 19.1614C2.21628 19.1442 2.39018 19.0902 2.54771 19.0027C2.70524 18.9153 2.84299 18.7963 2.95234 18.6532L9.27407 10.8098C9.43836 10.5679 9.5167 10.2779 9.49658 9.98627Z"
                fill="currentcolor"
              />
            </svg>
          </button>
        </div>
      </div>
      <div class="reviews-bottom">
        <div class="reviews-wrapper" :style="{transform: `translateX(${-33 + -1 * counter * 17}%)`, transition: 'all 1s ease-in'}">
            <div class="reviews-items" v-for="item, idx in clonedItems" :key="idx">
                <div class="item-top">
                    <img :src="require('@/assets/Content/FourReviews/' +item.img1)" alt="">
                    <div class="item-top-center">
                        <h2>{{item.name}}</h2>
                        <p>{{item.title}}</p>
                    </div>
                    <div class="item-top-right">
                        <button class="star" value="1" @click="selectStar(1)">&#9734;</button>
                        <button class="star" value="2" @click="selectStar(2)">&#9734;</button>
                        <button class="star" value="3" @click="selectStar(3)">&#9734;</button>
                        <button class="star" value="4" @click="selectStar(4)">&#9734;</button>
                        <button class="star" value="5" @click="selectStar(5)">&#9734;</button>
                    </div>
                </div>
                <div class="item-bottom">
                    <img :src="require('@/assets/Content/FourReviews/' + item.img2)" alt="" class="img-one">
                    <img :src="require('@/assets/Content/FourReviews/' + item.img2)" alt="" class="img-two">
                    <span>{{item.descript}}</span>
                </div>
            </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "bima-reviews",
  data() {
    return {
      reviews: [
        {
          id: 1,
          img1: "img1.png",
          img2: "Vector.png",
          name: "Дилшод Назаров",
          title: "Олимпийский чемпион",
          rating: 5,
          descript:
            "Чтобы избежать лишних финансовых затрат, я застраховал квартиру полисом “Салом, Сосед!” где сумма выплаты в случае затопа, пожара или кражи может гарантировано достигать до 40 000 сомони.Уверен, что взглянув на выгоду полиса и вы сделаете правильный выбор. Я доверяю полису “Салом, Сосед!” и вам советую!",
        },
        {
          id: 2,
          img1: "img2.png",
          img2: "Vector.png",
          name: "Дилшод Джураев",
          title: "Учредитель “55 group”",
          rating: 4,
          descript:
            "Дилшод Джураев - предприниматель, учредитель “55 group”. Выбор страхового полиса - важное дело, к которому Дилшод относится серьезно.Он решил остановить свой выбор на удобном и быстром страховании своего имущества и приобрел страховой полис “Салом, Сосед!” откомпании BIMA",
        },
      ],
      stars: null,
      counter: 0
    };
  },
  computed:{
    items(){
        return JSON.parse(JSON.stringify(this.reviews))
    },
    clonedItems(){
        return [...this.items, ...this.reviews, ...this.items]
    }
  },
  methods:{
    moveLeft(){
        if(this.counter < this.reviews.length-1){
            this.counter++
        }else{
            this.counter=0
        }
    },
    moveRight(){
        if(this.counter <= 0){
            this.counter = this.reviews.length-1
        }else{
            this.counter--
        }
    },
    selectStar(e){
        let stars = document.querySelectorAll('.star')

        stars.forEach(elem=>{
            if(elem.value <= e){
                if(elem.classList.contains('deactive')){
                    elem.classList.remove('deactive')
                    elem.classList.add('active')
                }else{
                    elem.classList.add('active')
                }
            }else{
                if(elem.classList.contains('active')){
                    elem.classList.remove('active')
                    elem.classList.add('deactive')
                }else{
                    elem.classList.add('deactive')
                }
            }
        })
    }
  }
};
</script>
