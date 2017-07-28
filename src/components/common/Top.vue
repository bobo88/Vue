<!--
内容：公共头部
作者：BOBO
日期： 20170728
-->
<template>
  <div class="top">
    <h3 class="tit-cont-wrap"><span>我是头部内容</span></h3>
  </div>
</template>

<script>
export default {
  name: 'top',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.tit-cont-wrap{ position: absolute; z-index: 3; top: 0; left: 0; width: 100%; height: 90px; line-height: 90px; color: #fff; font-size: 24px; background: #46576B; text-align: center;}
</style>
