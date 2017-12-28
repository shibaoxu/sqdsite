<template>
  <div class="navbar" :class="{fix}">
    <div class="navbar-container">
      <div class="logo">
        <img src="" >
      </div>
      <ul class="navbar-list">
        <li>首页</li>
        <li>产品</li>
        <li>解决方案</li>
        <li>关于我们</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'navbar',
  data () {
    return {
      fix: false
    }
  },
  methods: {
    handleWindowScroll (e) {
      this.fix = window.scrollY > 0
    }
  },
  beforeMount () {
    window.addEventListener('scroll', this.handleWindowScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', null)
  }
}
</script>

<style>

</style>
