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
		
		<!-- 图表内容 -->
		<div class="chart-wrap clearfix">
		    <div class="left-box fl">
		        <!-- 最近7天收入趋势 -->
				<last7-days class="left-box-item left-box-top"></last7-days>

		        <!-- 今日top3 -->
		        <today-top3 class="left-box-item left-box-bottom"></today-top3>
		    </div>

		    <div class="right-box fr">
		        <h4 class="income-source-tit clearfix">酒店收入分布 <a href="#" class="fr">查看其他指标</a></h4>

		        <div class="income-source-cont">
		            <table cellpadding="0" cellspacing="0">
		                <thead>
		                    <tr>
		                        <th rowspan="2">经营分类</th>
		                        <th colspan="4" class="tc">当日</th>
		                        <th colspan="4" class="tc">本月累计</th>
		                        <th colspan="4" class="tc">本年累计</th>
		                    </tr>
		                    <tr>
		                        <th>实际</th>
		                        <th>日预算</th>
		                        <th>完成率</th>
		                        <th>同比</th>

		                        <th>实际</th>
		                        <th>日预算</th>
		                        <th>完成率</th>
		                        <th>同比</th>

		                        <th>实际</th>
		                        <th>日预算</th>
		                        <th>完成率</th>
		                        <th>同比</th>
		                    </tr>
		                </thead>
		                <tbody>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                    <tr>
		                        <td class="left-tit">内部管理酒店</td>
		                        <td>111</td>
		                        <td>222</td>
		                        <td>333</td>
		                        <td>444</td>

		                        <td>555</td>
		                        <td>666</td>
		                        <td>777</td>
		                        <td>888</td>

		                        <td>999</td>
		                        <td>000</td>
		                        <td>222</td>
		                        <td>333</td>
		                    </tr>
		                </tbody>
		            </table>
		        </div>
		    </div>
		</div><!-- .chart-wrap -->
	</div>
</template>

<script>
import overviewOfIncome from '@/components/daily/overviewOfIncome'
import last7Days from '@/components/daily/last7Days'
import todayTop3 from '@/components/daily/todayTop3'

export default {
	components: {
		overviewOfIncome,
		last7Days,
		todayTop3
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

	/* chart-wrap: 最近7天收入趋势 & 今日top3 & 酒店指标明细 */
	.chart-wrap{
		.left-box{ width: 40%; height: 520px;
			.left-box-item{ width: 100%; height: 250px; border: 1px solid rgba(43,60,80,0.08); box-shadow: 0 2px 4px 0 rgba(0,0,0,0.06); border-radius: 4px;
				&.left-box-top{ margin-bottom: 20px;}
			}
		}
		.right-box{ padding: 15px; width: 58%; height: 520px; border: 1px solid rgba(43,60,80,0.08); box-shadow: 0 2px 4px 0 rgba(0,0,0,0.06); border-radius: 4px;
			.income-source-tit{ margin-bottom: 10px; height: 25px; line-height: 25px; font-size: 14px; color: #344559; letter-spacing: 1px;
				a{ font-size: 12px; color: #4A90E2; letter-spacing: 0.86px;}
			}
			.tc{ text-align: center;}
			.income-source-cont{ width: 100%; height: 450px; overflow: auto;
				table{ width: 100%; border: 1px solid #eee;
					thead{ background: #f9f9f9;
						tr{ line-height: 30px;}
						th{ padding: 0 10px; border-right: 1px solid #eee; text-align: center;}
					}
					tr{ line-height: 36px; border-bottom: 1px solid #eee;
						td{ padding: 0 10px; min-width: 80px; border-right: 1px solid #eee; text-align: center;}
						.left-tit{ min-width: 140px;}
					}
				}
			}
		}
	}
</style>
