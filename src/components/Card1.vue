<template>
  <div class="card1">
    <div class="card1-icon"><Icon :type="content.icon" /></div>
    <h1 class="card1-title">{{ content.title }}</h1>
    <div class="card1-detail">
      {{ content.desc }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'card1',
  props: ['content']

}
</script>

<style>

</style>
