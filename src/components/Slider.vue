<template>
        <div class="slider">
            <div class="slider__container container">
                <swiper class="slider__slider"
                    :modules="modules"
                    :slides-per-view="1"
                    :space-between="50"
                    parallax
                    grabCursor
                    navigation
                    :pagination="{ clickable: true }"
                    :scrollbar="{ draggable: true }"
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                >
                    <swiper-slide class="slider__slide" v-for="slide in sliders" :key="slide.id">
                        <div class="slider__body" :style="{ backgroundImage: `url('${slide.image}')`}">
                            <div class="slider__content content-slider">
                                <div class="content-slider__data">*Акция действует до {{slide.data}}</div>
                                <div class="content-slider__title">{{slide.title}}</div>
                                <div class="content-slider__text">{{slide.more}}</div>
                                <button class="content-slider__button">ПРИНЯТЬ УЧАСТИЕ</button>
                            </div>
                        </div>
                    </swiper-slide>
                </swiper>
            </div>
        </div>
</template>
<script>
  // import Swiper core and required modules
    import SwiperCore, { Navigation, Pagination, Scrollbar, A11y, Parallax } from 'swiper';

  // Import Swiper Vue.js components
    import { Swiper, SwiperSlide } from 'swiper/vue';

//   Import Swiper styles
    import 'swiper/swiper.scss';
    import 'swiper/components/navigation/navigation.scss';
    import 'swiper/components/pagination/pagination.scss';
    // import 'swiper/scss/scrollbar';

  // Import Swiper styles
    SwiperCore.use([Navigation, Parallax, Pagination])
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
                sliders:[
                    {
                        id: 1,
                        title: 'Название',
                        more: 'Условия акции в пару строк, Условия акциив пару строк, Условия акции в пару строк',
                        image: require('@/assets/img/slider.png'),
                        data: '04/09/22'
                    },
                    {
                        id: 1,
                        title: 'Название',
                        more: 'Условия акции в пару строк, Условия акциив пару строк, Условия акции в пару строк',
                        image: require('@/assets/img/slider.png'),
                        data: '04/09/22'
                    }
                ],
                str:'hello world'
        
            }
        },
        methods:{
            obSpan(){
                var res = this.str.split('');
                console.log(res,'res');
            }
        }

    };
</script>
<style lang="scss">
.swiper-button-prev, .swiper-button-next{
    width: 67px;
    height: 67px;
    border-radius: 50%;
    background-color: #fff;
    font-family: 'i-bold';
    &::after{
        font-size: 16px;
        color: #FFC85E;
    }
}
.swiper-button-prev{
    left: -28px;
    z-index: 5;
}
.swiper-button-next{
    right: -28px;
    z-index: 5;
}
.slider {
    margin-bottom: 100px;

		// .slider__container

		&__container {
		}

		// .slider__slider

		&__slider {
		}

		// .slider__slide

		&__slide {
            border-radius: 10px;
            // overflow: hidden;
		}

		// .slider__content

		&__content {
            padding: 80px 0px 0px 113px;
            color: #fff;
		}

		// .slider__body

		&__body {
		}
}

.content-slider {

		// .content-slider__data

		&__data {
            font-size: 14px;
            letter-spacing: 3px;
            margin-bottom: 10px;
		}

		// .content-slider__title

		&__title {
            font-size: 70px;
            font-weight: 500;
            line-height: 110%;
            font-family: 'i-bold';
            margin-bottom: 35px;
            max-width: 576px;
            & span{
                font-size: 70px;
            }
		}

		// .content-slider__text

		&__text {
            max-width: 498px;
            font-size: 20px;
            line-height: 150%;
            font-weight: 400;
            margin-bottom: 50px;
		}

		// .content-slider__button

		&__button {
            background-color: #FFC85E;
            color: #fff;
            font-style: 18px;
            padding: 34px;
            width: 343px;
            border-radius: 79px;
            border: unset;

		}
}


.slider__body{
    padding-bottom: 77px;
    height: 500px;
    background-repeat: no-repeat;
    // background-size: cover;
    background-position: right;

}
.slider__slide{
    background: linear-gradient(0deg, #B7BFCA 0%, #BDC7D0 65.9%, #BDC7D1 100%);
}
</style>