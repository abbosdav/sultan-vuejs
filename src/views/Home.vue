<template>
  <div class="home">
      <Banner/>
      <Products/>
      <Category/>
      <Slider/>
  </div>
</template>

<script>

import Banner from '../components/Banner.vue'
import Products from '../components/Products.vue'
import Category from '../components/Category.vue'
import Slider from '../components/Slider.vue'

export default {
  name: 'Home',
  components: {
    Banner,
    Products,
    Category,
    Slider
  },
  data(){
    return{
      
    }
  }
}
</script>