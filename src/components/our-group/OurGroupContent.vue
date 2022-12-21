<template>
    <div class="our-group-content">
        <div class="our-group-wrapper">
            <div class="group-items" v-for="item, idx in group" :key="idx">
                <img :src="require('@/assets/OurGroup/Content/' + item.img)" alt="">
                <div class="item-title">
                    <h5>{{item.name}}</h5>
                <p>{{item.position}}</p>
                </div>
                <div class="item-mail">
                    <img src="@/assets/OurGroup/Content/img1.svg" alt="">
                    <span>{{item.mail}}</span>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'our-group',
    data(){
        return{
            group:[
                {
                    id: 1,
                    img: 'img1.png',
                    name: 'Чулибаев Вафо',
                    position: 'Генеральный директор',
                    mail: 'vchulibaev@bima.tj'
                },
                {
                    id: 2,
                    img: 'img2.png',
                    name: 'Бамахрама Азиз',
                    position: 'Исполнительный директор',
                    mail: 'abamakhrama@bima.tj'
                },
                {
                    id: 3,
                    img: 'img3.png',
                    name: 'Хайдаров Садмухтор',
                    position: 'Административный директор',
                    mail: 'shaydarov@bima.tj'
                },
                {
                    id: 4,
                    img: 'img4.png',
                    name: 'Сулеймонов Акмал',
                    position: 'Начальник отдела по работе с корпоративными клиентами',
                    mail: 'asuleymonov@bima.tj'
                },
                {
                    id: 5,
                    img: 'img5.png',
                    name: 'Муниева Полина',
                    position: 'Начальник отдела маркетинга и координации Call центра',
                    mail: 'pmunieva@bima.tj'
                },
                {
                    id: 6,
                    img: 'img6.png',
                    name: 'Вахобов Абдуазизхон',
                    position: 'Начальник отдела управления рисками и перестрахования',
                    mail: 'avakhobov@bima.tj'
                },
                {
                    id: 7,
                    img: 'img7.png',
                    name: 'Расулов Ильхом',
                    position: 'Начальник отдела сервиса ДМС',
                    mail: 'rasulov@bima.tj'
                },
                {
                    id: 8,
                    img: 'img8.png',
                    name: 'Изатуллоева Кибриё',
                    position: 'Начальник отдела бухгалтерского учета и отчетности',
                    mail: 'kizatulloeva@bima.tj'
                }
            ]
        }
    }
}
</script>