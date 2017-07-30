<!--
内容：最近7天收入趋势 组件
作者：BOBO
日期： 20170728
-->
<template>
	<div class="today-top3" id="todayTop3">
		
	</div>
</template>

<script>
import echarts from 'echarts'

export default {
	name: 'today-top3',
	data () {
		return {
		  	msg: ''
		}
	},
	mounted(){
		this.$nextTick(function() {
            var last7DaysChart = echarts.init(document.getElementById('last7Days'));
            var last7DaysOption = {
                title: {
                    text: '最近7天收入趋势',
                    top: 10,
                    left: 10,
                    textStyle: {
                        color: '#344559',
                        fontSize: 14,
                        fontWeight: 'normal'
                    }
                },
                tooltip : {
                    trigger: 'axis'
                },
                color:['#48cda6','#fd87ab','#11abff'],  //手动设置每个图例的颜色
                legend: {
                    top: 10,
                    right: 10,
                    itemHeight: 8,
                    textStyle:{
                        color: '#666',
                    },
                    data:['本日','上年同期','日预算']
                },
                toolbox: {
            
                },
                calculable : true,
                xAxis : [
                    {  
                        splitLine:{show: false}, //去除网格线
                        type : 'category',
                        boundaryGap : false,
                        data : ['06-22','06-23','06-24','06-25','06-26','06-27','06-28']
                    }
                ],
                yAxis : [
                    {
                        splitLine:{
                            lineStyle: {
                                color: '#eee'
                            }
                        },
                        type : 'value'
                    }
                ],
                series : [
                    {
                        name:'本日',
                        type:'line',
                        stack: '总量',
                        data:[120, 132, 101, 134, 90, 230, 210]
                    },
                    {
                        name:'上年同期',
                        type:'line',
                        stack: '总量',
                        data:[220, 182, 191, 234, 290, 330, 310]
                    },
                    {
                        name:'日预算',
                        type:'line',
                        stack: '总量',
                        data:[150, 232, 201, 154, 190, 330, 410]
                    }
                ]
            };
            // 使用刚指定的配置项和数据显示图表。
            last7DaysChart.setOption(last7DaysOption);
        })
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

</style>
