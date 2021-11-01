<template>
  <div id="nav">
    <div class="header">
      <Header></Header>
    </div>
    <div class="sections">
      <!-- Pages -->
      <router-view/> 
    </div>
    <div class="footer">
      <Footer></Footer>
    </div>
  </div>
</template>

<script>
import Header from '@/layouts/Header.vue'
import Footer from '@/layouts/Footer.vue'
export default {
  components:{
    Header,
    Footer
  }
}
</script>

<style lang="scss">
.sections{
  
}
</style>
