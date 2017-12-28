<template>
  <Carousel v-model="index">
    <CarouselItem>
      <div>
        <img src="/static/images/banner_express_feature.jpg" >
      </div>
    </CarouselItem>
  </Carousel>
</template>

<script>
export default {
  name: 'banner',
  data () {
    return {
      index: 0
    }
  }
}
</script>

<style>

</style>
