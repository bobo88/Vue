<!--
内容：公共左侧栏
作者：BOBO
日期： 20170728
-->
<template>
  <div class="left-cont-wrap">
      <div class="left-cont">
         <span>我是左侧内容</span> 
      </div>
  </div>
</template>

<script>
export default {
  name: 'left',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.left-cont-wrap{ position: absolute; z-index: 2; top: 0; left: 0; padding-top: 90px; padding-right: 10px; width: 250px; height: 100%; min-height: 100vh; color: #000; font-size: 24px; text-align: center;
	.left-cont{ position: relative; z-index: 1; width: 100%; height: 100%; background: #eee;
		span { position: absolute; z-index: 4; top: 50%; display: block; width: 100%; padding: 0 10px; -webkit-transform: translateY(-50%); transform: translateY(-50%);}
	}
}
</style>
