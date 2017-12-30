<template>
  <Carousel v-model="index" class="pc-banner">
    <CarouselItem>
      <div class="banner-item">
        <img src="/static/images/banner_express_feature.jpg" >
      </div>
    </CarouselItem>
  </Carousel>
</template>

<script>
export default {
  name: 'banner',
  props: ['bannerItems'],
  data () {
    return {
      index: 0
    }
  }
}
</script>

<style>

</style>
