<template>
  <div class="navbar" :class="{fix}">
    <div class="navbar-container">
      <div class="logo">
        <img :src="logo" >
      </div>
      <Dropdown class="dropdown" placement="bottom-end" :transfer="true">
        <a href="javascript:void(0)">
            <Icon type="navicon-round"></Icon>
        </a>
        <DropdownMenu slot="list">
            <DropdownItem v-for="item in menus" :name="item.name" :key="item.name">{{ item.title }}</DropdownItem>
        </DropdownMenu>
      </Dropdown>

      <ul class="navbar-list">
        <li v-for="item in menus" :key="item.name"><a :href="item.path"> {{ item.title }}</a></li>
      </ul>

    </div>
  </div>
</template>

<script>
export default {
  name: 'navbar',
  props: ['logo', 'menus'],
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
