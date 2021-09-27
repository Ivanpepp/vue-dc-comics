<template>
  <div class="banner">
    <img :src="thumb" :alt="series">
    <h3>{{series}}</h3>
  </div>    
</template>

<script>

export default {
    name: 'Banner',
    props:{
        thumb: String,
        series: String
    }
}
</script>

<style lang='scss' scoped>
    @import '../style/variables.scss';
    .banner{
      width: calc(90% /6);
      img{
        object-position: center;
        object-fit: cover;
        margin-bottom: 10px;
        width: 200px;
        height: 200px;
      }
      h3{
        margin-bottom: 40px;
      }
    }
</style>