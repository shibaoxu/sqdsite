<template>
  <div class="home">    
  <Carousel v-model="index" class="pc-banner">
    <CarouselItem v-for="banner in homeData.pcBanners" :key="banner.name">
      <div class="banner-item" :style="`background-image: url(${banner.backgroundImage})`">
        <!-- <img src="/static/images/banner_express_feature.jpg" > -->
      </div>
    </CarouselItem>
  </Carousel>
  <div class="mobile-banner">
    <img src="/static/images/banner_express_mobile.png">
  </div>
  <div class="long-content">I am long content</div>
  </div>
</template>

<script>
import config from '@/config.json'
export default {
  name: 'home',
  data () {
    return {
      index: 0,
      homeData: config.home
    }
  },
  methods: {
  },
  components: {
  }

}
</script>

<style lang="postcss" scoped>
#banner1 {
  background-image: url("/static/images/banner_express_feature.jpg");
  width: 100%;
  height: 50em;
}
</style>
