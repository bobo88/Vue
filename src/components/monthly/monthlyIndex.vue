<!--
内容：日报页面 ~ 集团日报页面
作者：BOBO
日期： 20170728
-->
<template>
	<div class="monthly-index">
		<!-- 日期模块 -->
		<div class="date-module">
			<Row>
				<Col span="12">
					<Date-picker type="date" placeholder="选择日期" style="width: 200px"></Date-picker>
				</Col>
			</Row>
		</div>
		
		<!-- 图表内容 -->
		<div class="chart-wrap clearfix">
		    <div class="left-box fl">
		        <!-- 财务运营KPI -->
		        <financial-operation class="pb-box-item mb20"></financial-operation>

		        <!-- 经营收入月度趋势分析 -->
		        <analysis-income class="pb-box-item mb20"></analysis-income>
		    </div>

		    <div class="right-box fr">
		    	<!-- 增收节支成效 -->
		    	<increase-revenue-results class="pb-box-item mb20"></increase-revenue-results>

		    	<!-- 财务能力 -->
		        <financial-capability class="pb-box-item mb20"></financial-capability>
		    </div>
		</div><!-- .chart-wrap -->
	</div>
</template>

<script>
import financialOperation from '@/components/monthly/monthlyComponents/financialOperation'
import analysisIncome from '@/components/monthly/monthlyComponents/analysisIncome'
import increaseRevenueResults from '@/components/monthly/monthlyComponents/increaseRevenueResults'
import financialCapability from '@/components/monthly/monthlyComponents/financialCapability'

export default {
	components: {
		financialOperation,
		analysisIncome,
		increaseRevenueResults,
		financialCapability
	},
  	name: 'monthly-index',
  	data () {
		return {
			msg: ''
		}
  	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
	.monthly-index{ padding-right: 20px;}
	.date-module{ padding: 10px 0; width: 200px; height: 55px; line-height: 35px;}

	/* chart-wrap: 最近7天收入趋势 & 今日top3 & 酒店指标明细 */
	.chart-wrap{
		.mb20{ margin-bottom: 20px;}
		.pb-box-item{ width: 100%; height: 360px; border: 1px solid rgba(43,60,80,0.08); box-shadow: 0 2px 4px 0 rgba(0,0,0,0.06); border-radius: 4px;}
		.left-box{ width: 53%;}
		.right-box{ width: 45%;}
	}
</style>
