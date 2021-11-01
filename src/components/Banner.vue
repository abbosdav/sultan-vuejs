<template>
      <div class="home__banner" :style="{backgroundImage}">
      <div class="home__shadow">
        <div class="home__container container">
        <div class="home__content content-home">
          <div class="content-home__title">Бытовая химия, косметика хозтовары</div>
          <div class="content-home__text">оптом по кокчетаву и области</div>
          <button class="content-home__button">В КАТАЛОГ</button>
          <div class="content-home__services">
            <a class="content-home__servic service-home">
              <span class="service-home__button">+</span>
              <span class="service-home__text">Только самые выгодные предложения</span>
            </a>
            <a class="content-home__servic service-home">
              <span class="service-home__button">+</span>
              <span class="service-home__text">Бесплатная доставка по Кокчетаву от 10 тыс ₸</span>
            </a>
          </div>
        </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
    data() {
        return{
            backgroundImage: `url(${require('@/assets/img/section.png')})`
        }
        
    },
}
</script>
<style lang="scss" scoped>
  .home {

		// .home__banner
		&__banner {
      height: 796px;
      width: 100%;
      background-size: cover;
      background-repeat: no-repeat;
      position: relative;
      &::after{
        content: '';
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        width: 45%;
        display: block;
        background: linear-gradient(89.86deg, #8A94AB 0.13%, rgba(138, 148, 171, 0) 99.89%);
        z-index: 1;
      }
		}
		// .home__content

		&__content {
      position: relative;
      z-index: 5;
		}
}
.container {
}
.content-home {

  // .content-home__title

  &__title {
    max-width: 570px;
    padding-top: 98px;
    color: #fff;
    font-size: 70px;
    line-height: 77/70*100%;
  }

  // .content-home__text

  &__text {
    font-size: 30px;
    color: #fff;
    max-width: 551px;
    margin-top: 40px;
    font-weight: 700;
  }

  // .content-home__button

  &__button {
    background: #FFC85E;
    color: #fff;
    border: unset;
    padding: 30px;
    border-radius: 79px;
    width: 300px;
    margin-top: 60px;
  }

  // .content-home__services

  &__services {
    margin-top: 127px;
    display: flex;
  }

  // .content-home__servic

  &__servic {
    padding-right: 35px;
  }
}
.service-home {
  display: flex;
  align-items: center;

  // .service-home__button
  &__button {
    width: 35px;
    height: 35px;
    border-radius: 50%;
    background-color: #FFC85E;
    color: #fff;
    display: inline-block;
    text-align: center;
    padding-top: 6px;
  }

  // .service-home__text

  &__text {
    display: inline-block;
    max-width: 178px;
    color: #fff;
    line-height: 150%;
    font-size: 14px;
    margin-left: 10px;
  }
}

</style>