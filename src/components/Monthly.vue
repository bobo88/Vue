<!--
内容：月报页面入口
作者：BOBO
日期： 20170731
-->
<template>
  <div class="monthly">
  	<router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'monthly',
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
