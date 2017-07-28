<!--
内容：收入总览页面
作者：BOBO
日期： 20170728
-->
<template>
	<div class="overview-of-income">
		<h3 class="tit">收入总览</h3>
		
		<div class="income-list">
			<Row>
		        <Col span="8" class="today-income">
		        	<Row>
	        	        <Col span="12">今日</Col>
	        	        <Col span="8">{{ todayIncome.incomeNum | currencyFormatter }}</Col>
	        	        <Col span="4"></Col>
	        	    </Row>
	        	    <Row>
	        	        <Col span="12">同比</Col>
	        	        <Col span="8">{{ todayIncome.Yoy.val | currencyFormatter }}</Col>
	        	        <Col span="4">
	        	        	<state-icon :state="todayIncome.Yoy.state"></state-icon>
	        	        </Col>
	        	    </Row>
	        	    <Row>
	        	        <Col span="12">环比</Col>
	        	        <Col span="8">{{ todayIncome.Mom.val }}</Col>
	        	        <Col span="4">
							<state-icon :state="todayIncome.Mom.state"></state-icon>
	        	        </Col>
	        	    </Row>
	        	    <Row>
	        	        <Col span="12">预算完成率</Col>
	        	        <Col span="8">{{ todayIncome.budgetCompletionRate.val }}%</Col>
	        	        <Col span="4">
							<state-icon :state="todayIncome.budgetCompletionRate.state"></state-icon>
	        	        </Col>
	        	    </Row>
		        </Col>
		        <Col span="8" class="month-income">
    	        	<Row>
            	        <Col span="12">本月累计</Col>
            	        <Col span="8">{{ monthIncome.incomeNum | currencyFormatter }}</Col>
            	        <Col span="4"></Col>
            	    </Row>
            	    <Row>
            	        <Col span="12">同比</Col>
            	        <Col span="8">{{ monthIncome.Yoy.val | currencyFormatter }}</Col>
            	        <Col span="4">
							<state-icon :state="monthIncome.Yoy.state"></state-icon>
            	        </Col>
            	    </Row>
            	    <Row>
            	        <Col span="12">月度预算完成率</Col>
            	        <Col span="8">{{ monthIncome.monthlyBudgetCompletionRate.val }}%</Col>
            	        <Col span="4">
							<state-icon :state="monthIncome.monthlyBudgetCompletionRate.state"></state-icon>
            	        </Col>
            	    </Row>
            	    <Row>
            	        <Col span="12">时间进度</Col>
            	        <Col span="8">{{ monthIncome.timeSchedule.val }}%</Col>
            	        <Col span="4">
							<state-icon :state="monthIncome.timeSchedule.state"></state-icon>
            	        </Col>
            	    </Row>
		        </Col>
		        <Col span="8" class="year-income">
    	        	<Row>
            	        <Col span="12">本年累计</Col>
            	        <Col span="8">{{ yearIncome.incomeNum | currencyFormatter }}</Col>
            	        <Col span="4"></Col>
            	    </Row>
            	    <Row>
            	        <Col span="12">同比</Col>
            	        <Col span="8">{{ yearIncome.Yoy.val | currencyFormatter }}</Col>
            	        <Col span="4">
							<state-icon :state="yearIncome.Yoy.state"></state-icon>
            	        </Col>
            	    </Row>
            	    <Row>
            	        <Col span="12">年度预算完成率</Col>
            	        <Col span="8">{{ yearIncome.annualBudgetCompletionRate.val }}%</Col>
            	        <Col span="4">
							<state-icon :state="yearIncome.annualBudgetCompletionRate.state"></state-icon>
            	        </Col>
            	    </Row>
            	    <Row>
            	        <Col span="12">时间进度</Col>
            	        <Col span="8">{{ yearIncome.timeSchedule.val }}%</Col>
            	        <Col span="4">
							<state-icon :state="yearIncome.timeSchedule.state"></state-icon>
            	        </Col>
            	    </Row>
		        </Col>
		    </Row>
		</div>
	</div>
</template>

<script>
import axios from 'axios'
//引入全局过滤器
import currencyFormatter from '@/filter/currencyFormatter'
//引入状态组件
import StateIcon from '@/components/common/StateIcon'

export default {
	components: {
		StateIcon
	},
  	name: 'overview-of-income',
  	data () {
		return {
			msg: '收入总览',
			todayIncome: { // 注意： vue读取返回的json嵌套数据，需要在最开始的 data属性中设置 这些变量，否则会读取报错。data中设置一个缺省值即可。
				"incomeNum": '',
				"Yoy": {
				  "val": '',
				  "state": ''
				},
				"Mom": {
				  "val": '',
				  "state": ''
				},
				"budgetCompletionRate": {
				  "val": '',
				  "state": ''
				}
			},
			monthIncome: {
				"incomeNum": '',
				"Yoy": {
				  "val": '',
				  "state": ''
				},
				"monthlyBudgetCompletionRate": {
				  "val": '',
				  "state": ''
				},
				"timeSchedule": {
				  "val": '',
				  "state": ''
				}
			},
			yearIncome: {
				"incomeNum": '',
				"Yoy": {
				  "val": '',
				  "state": ''
				},
				"annualBudgetCompletionRate": {
				  "val": '',
				  "state": ''
				},
				"timeSchedule": {
				  "val": '',
				  "state": ''
				}
			}
		}
  	},
  	//钩子函数: 异步加载数据
  	mounted: function(){
  		var that = this;
  		// 注意： 访问服务器文件，应该把json文件放在最外层的static文件夹，这个文件夹是vue-cli内置服务器向外暴露的静态文件夹
		axios.get('/static/overviewIncome.json')
			.then(function (response) {
				if (response.data.code == 1) {
					that.$nextTick(function () {
					    that.todayIncome = response.data.todayIncome;
					    that.monthIncome = response.data.monthIncome;
					    that.yearIncome = response.data.yearIncome;
					})
				}
			})
			.catch(function (error) {
				console.log(error);
			});
  	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
	/* 收入总览 */
	.overview-of-income{ margin-bottom: 20px; padding: 15px 20px;background: #FFFFFF; border: 1px solid rgba(43,60,80,0.08); box-shadow: 0 2px 4px 0 rgba(0,0,0,0.06); border-radius: 4px;
		.tit{ height: 30px; line-height: 30px; color: #344559; font-size: 14px;}
		.income-list{ padding: 10px 0; line-height: 30px; color: #666; letter-spacing: 0.5px;
			.theme{ color: #333; font-size: 14px;}
			.icon{ font-size: 20px;}
			.today-income{ padding-left: 20px; border-right: 1px solid #eee;}
			.month-income{ padding-left: 20px; border-right: 1px solid #eee;}
			.year-income{ padding-left: 20px;}
		}
	}
</style>
