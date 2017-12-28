<template>
  <div class="home">
    <Navbar />
    <Banner />
    <div class="long-content">I am long content</div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Banner from '@/components/Banner'
export default {
  name: 'home',
  methods: {
  },
  components: {
    Navbar,
    Banner
  }

}
</script>

<style>

</style>
