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
        <li><a href="/">首页</a></li>        
        <li class="dropdown">
          <span>产品</span>
          <div class="dropdown-content">
            <div class="dropdown-arrow"></div>
            <div class="dropdown-menu">
              <Card2 icon="/static/images/logos/x1.png" title="SQD X" subtitle="私有云平台" details="SQD X帮助用户构建基于OpenStack标准的企业级私有云平台， 能够提供IaaS层和PaaS层资源， 同时具备资源编排、多级权限、全面监控、计费报表等增强特性。" />
              <Card2 icon="/static/images/logos/fusion.png" title="SQD X" subtitle="私有云平台" details="SQD X帮助用户构建基于OpenStack标准的企业级私有云平台， 能够提供IaaS层和PaaS层资源， 同时具备资源编排、多级权限、全面监控、计费报表等增强特性。" />
              <Card2 icon="/static/images/logos/one.png" title="SQD X" subtitle="私有云平台" details="SQD X帮助用户构建基于OpenStack标准的企业级私有云平台， 能够提供IaaS层和PaaS层资源， 同时具备资源编排、多级权限、全面监控、计费报表等增强特性。" />
            </div>
          </div>
        </li>
        <li class="dropdown">
          <span>解决方案</span>
          <div class="dropdown-content">
            <div class="dropdown-arrow"></div>
            <div class="dropdown-menu">
              <Card2 icon="/static/images/logos/x1.png" title="SQD X" subtitle="私有云平台" details="SQD X帮助用户构建基于OpenStack标准的企业级私有云平台， 能够提供IaaS层和PaaS层资源， 同时具备资源编排、多级权限、全面监控、计费报表等增强特性。" />
              <Card2 icon="/static/images/logos/fusion.png" title="SQD X" subtitle="私有云平台" details="SQD X帮助用户构建基于OpenStack标准的企业级私有云平台， 能够提供IaaS层和PaaS层资源， 同时具备资源编排、多级权限、全面监控、计费报表等增强特性。" />
              <Card2 icon="/static/images/logos/one.png" title="SQD X" subtitle="私有云平台" details="SQD X帮助用户构建基于OpenStack标准的企业级私有云平台， 能够提供IaaS层和PaaS层资源， 同时具备资源编排、多级权限、全面监控、计费报表等增强特性。" />
            </div>
          </div>
        </li>
        <li><a href="/about">关于</a></li>
        
      </ul>
      
    </div>
  </div>
</template>

<script>
import Card2 from '@/components/Card2'
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
  },
  components: {
    Card2
  }
}
</script>

<style>

</style>
