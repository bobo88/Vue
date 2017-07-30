<!--
内容：日报页面 ~ 酒店日报页面
作者：BOBO
日期： 20170730
-->
<template>
	<div class="hotel-daily">
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
		
		<!-- 图表内容 -->
		<div class="chart-wrap clearfix">
		    <div class="left-box fl">
		        <!-- 最近7天收入趋势 -->
				<last7-days class="left-box-item left-box-top"></last7-days>

		        <!-- 今日top3 -->
		        <today-top3 class="left-box-item left-box-bottom"></today-top3>
		    </div>

		    <div class="right-box fr">
		    	<!-- 酒店指标明细 -->
		        <hotel-index-details></hotel-index-details>
		    </div>
		</div><!-- .chart-wrap -->
	</div>
</template>

<script>
import overviewOfIncome from '@/components/daily/dailyComponents/overviewOfIncome'
import last7Days from '@/components/daily/dailyComponents/last7Days'
import todayTop3 from '@/components/daily/dailyComponents/todayTop3'
import hotelIndexDetails from '@/components/daily/dailyComponents/hotelIndexDetails'

export default {
	components: {
		overviewOfIncome,
		last7Days,
		todayTop3,
		hotelIndexDetails
	},
  	name: 'hotel-daily',
  	data () {
		return {
			msg: ''
		}
  	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
	.hotel-daily{ padding-right: 20px;}
	.date-module{ padding: 10px 0; width: 200px; height: 55px; line-height: 35px;}

	/* chart-wrap: 最近7天收入趋势 & 今日top3 & 酒店指标明细 */
	.chart-wrap{
		.left-box{ width: 40%; height: 520px;
			.left-box-item{ width: 100%; height: 250px; border: 1px solid rgba(43,60,80,0.08); box-shadow: 0 2px 4px 0 rgba(0,0,0,0.06); border-radius: 4px;
				&.left-box-top{ margin-bottom: 20px;}
			}
		}
		.right-box{ padding: 15px; width: 58%; height: 520px; border: 1px solid rgba(43,60,80,0.08); box-shadow: 0 2px 4px 0 rgba(0,0,0,0.06); border-radius: 4px;
		}
	}
</style>
