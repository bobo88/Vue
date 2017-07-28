<!--
内容：公共状态指示组件（包括向上箭头、向下箭头、圆点）
作者：BOBO
日期： 20170728
-->
<template>
	<div class="state-icon">
		<i class="iconfont icon-up" v-if="state == 'up' "></i>
		<i class="iconfont icon-down" v-if="state == 'down' "></i>
		<i class="iconfont icon-yuandian" v-if="state == 'circle' "></i>
		<i class="iconfont icon-yuandian color-orange" v-if="state == 'warn-circle' "></i>
	</div>
</template>

<script>
export default {
  name: 'state-icon',
  props: ['state'],
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
