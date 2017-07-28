<!--
内容：日报页面入口
作者：BOBO
日期： 20170728
-->
<template>
  <div class="daily">
      <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'daily',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

</style>
