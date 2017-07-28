<!--
内容：日报页面 ~ 集团日报页面
作者：BOBO
日期： 20170728
-->
<template>
	<div class="group-daily">
		<!-- 日期模块 -->
		<div class="date-module">
			<Row>
				<Col span="12">
					<Date-picker type="date" placeholder="选择日期" style="width: 200px"></Date-picker>
				</Col>
			</Row>
		</div>

		<!-- 收入总览 -->
		<overview-of-income></overview-of-income>

	</div>
</template>

<script>
import overviewOfIncome from '@/components/daily/overviewOfIncome'

export default {
	components: {
		overviewOfIncome
	},
  	name: 'group-daily',
  	data () {
		return {
			msg: ''
		}
  	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
	.group-daily{ padding-right: 20px;}
	.date-module{ padding: 10px 0; width: 200px; height: 55px; line-height: 35px;}
</style>
