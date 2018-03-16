<template>
  <div class="home">    
  <Carousel v-model="index" class="pc-banner">
    <CarouselItem>
      <div class="banner-item" style="background-image: url(/static/images/home/banners/pcbanner-01.jpg)">
        <div class="banner-content">
          <h1 class="pcbanner-title">SQD 全端私有云 免费试用 极速体验</h1>
          <h2>如果你有以下私有云需求:</h2>
          <ul>
            <li>中小规模数据中心</li>
            <li>开发测试平台</li>
            <li>容灾备份平台</li>
          </ul>
          <h2>请即刻体验零基础上手，图形化操作的云平台。</h2>
          <p><Button>申请免费试用</Button>&nbsp;&nbsp;<small>我们会在24小时之内联系您</small></p>
        </div>
      </div>
    </CarouselItem>
    <CarouselItem>
      <div class="banner-item" style="background-image: url(/static/images/home/banners/pcbanner-02.jpg)">
        <div class="banner-content">
          <h1 class="pcbanner-title">SQD One 企业级容器平台</h1>
          <h2>如果你有以下需求:</h2>
          <ul>
            <li>应用快速交付，弹性部署</li>
            <li>落地devops交付流程</li>
            <li>传统业务互联网转型</li>
          </ul>
          <h2>请即刻体验零基础上手，图形化操作的容器云平台。</h2>
          <p><Button>申请免费试用</Button>&nbsp;&nbsp;<small>我们会在24小时之内联系您</small></p>
        </div>
      </div>
    </CarouselItem>
    
  </Carousel>
  <div class="mobile-banner" style="background-image: url(/static/images/home/banners/mobile-banner.jpg)">
    <div class="mobile-banner-content">
      <h1 class="mobile-banner-title">SQD 全端私有云</h1>
      <h2> 免费试用 极速体验</h2>
      <p><Button>申请免费试用</Button></p>
      <p><small>我们会在24小时之内联系您</small></p>
    </div>
  </div>
  <div class="band grey">
    <div class="card-container">
      <Card1 :content="card" v-for="card in productCards" :key="card.name" />
    </div>
  </div>
  <div class="band">
    <div class="band-title">这些客户选择了全端网络</div>
    <Cases />
  </div>
  </div>
</template>

<script>
import config from '@/config.json'
import Card1 from '@/components/Card1'
import Card2 from '@/components/Card2'
import Cases from '@/components/Cases'

export default {
  name: 'home',
  data () {
    return {
      index: 0,
      productCards: config.home.productCards
    }
  },
  methods: {
  },
  components: {
    Card1,
    Card2,
    Cases
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
