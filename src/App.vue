<template>
  <div id="app">
    <Navbar :logo="navbarData.logoImage" :menus="navbarData.menus"/>
    <router-view/>
    <Footer />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import config from '@/config.json'
import Footer from '@/components/Footer'
export default {
  name: 'app',
  data () {
    return {
      navbarData: config.navbar
    }
  },
  components: {
    Navbar,
    Footer
  }
}
</script>
