<template>
        <div class="category">
            <div class="category__container container">
                <div class="category__title">Категории <span>товаров</span></div>
                <div class="category__sub-title">10 000+ ходовых позиций по спецмальным ценам</div>
                <swiper class="category__slider slider-category"
                    :modules="modules"
                    :slides-per-view="5"
                    :space-between="50"
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                >
                    <swiper-slide v-for="slide in categories" :key="slide.id">
                        <a href="" class="slider-category__image">
                            <img :src="slide.img" alt="">
                        </a>
                        <div class="slider-category__title">{{slide.title}}</div>
                    </swiper-slide>
                </swiper>
            </div>
            {{rasm}}
        </div>
</template>
<script>
  // import Swiper core and required modules
    import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';

  // Import Swiper Vue.js components
    import { Swiper, SwiperSlide } from 'swiper/vue';

//   Import Swiper styles
    import 'swiper/swiper.scss';
    // import 'swiper/scss/pagination';
    // import 'swiper/scss/scrollbar';

  // Import Swiper styles
    export default {
        components: {
        Swiper,
        SwiperSlide,
        },
        setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            onSwiper,
            onSlideChange,
            modules: [Navigation, Pagination, Scrollbar, A11y],
        };
        },
        data(){
            return{
                categories:[
                    {
                        id: 1,
                        img: require('@/assets/img/category1.png'),
                        title: 'Бытовая химия'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category4.png'),
                        title: 'Косметика и гигиена'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category3.png'),
                        title: 'Бытовая химия'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category2.png'),
                        title: 'Товары для детей и мам'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category5.png'),
                        title: 'Бытовая химия'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category1.png'),
                        title: 'Бытовая химия'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category4.png'),
                        title: 'Бытовая химия'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category3.png'),
                        title: 'Бытовая химия'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category2.png'),
                        title: 'Бытовая химия'
                    },
                    {
                        id: 1,
                        img: require('@/assets/img/category5.png'),
                        title: 'Бытовая химия'
                    },
                ],
            }
        }
    };
</script>
<style lang="scss">
    .category {
        margin-bottom: 100px;

		// .category__container

		&__container {
		}

		// .category__title

		&__title {
            margin-bottom: 15px;
            color:  #FFC85E;
            font-family: 'i-bold';
            font-size: 40px;
            & span{
                font-size: 40px;
                color: #000;
            }
            
		}

		// .category__sub-title

		&__sub-title {
            color: #3F4E65;
            font-size: 20px;
            margin-bottom: 50px;
		}

		// .category__slider

		&__slider {
		}
}

.slider-category {

		// .slider-category__image

		&__image {
            height: 250px;
            display: block;
            background-color: rgb(248, 248, 239);
            border-radius: 20px;
            margin-bottom: 15px;
            position: relative;
            overflow: hidden;
            & img{
                width: 100%;
                position: absolute;
                left: 0;
                bottom: 0;
            }
		}

		// .slider-category__title

		&__title {
            text-align: center;
		}
}


</style>