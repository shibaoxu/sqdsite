<template>
  <div id="app">
    <Navbar :logo="navbarData.logoImage" :menus="navbarData.menus"/>
    <router-view/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import config from '@/config.json'

export default {
  name: 'app',
  data () {
    return {
      navbarData: config.navbar
    }
  },
  components: {
    Navbar
  }
}
</script>
