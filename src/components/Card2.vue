<template>
  <div class="card2">
    <div class="icon">
      <img :src="icon" alt="">
    </div>
    <div class="desc">
      <div class="title">
        <p>{{title}}</p>
        <p>{{subtitle}}</p>
      </div>
      <div class="details">{{ details }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'card2',
  props: ['icon', 'title', 'subtitle', 'details']
}
</script>

<style>

</style>
