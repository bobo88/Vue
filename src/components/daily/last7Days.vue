<!--
内容：最近7天收入趋势 组件
作者：BOBO
日期： 20170728
-->
<template>
	<div class="last-7-days" id="last7Days">
		
	</div>
</template>

<script>
import echarts from 'echarts'

export default {
	name: 'last-7-days',
	data () {
		return {
		  	msg: ''
		}
	},
	mounted(){
		this.$nextTick(function() {
            var todayTop3Chart = echarts.init(document.getElementById('todayTop3'));
            var todayTop3Option = {
                title: {
                    text: '今日top3',
                    top: 10,
                    left: 10,
                    textStyle: {
                        color: '#344559',
                        fontSize: 14,
                        fontWeight: 'normal'
                    }
                },
                tooltip : { // 提示框组件
                    trigger: 'axis'
                },
                grid: { // 直角坐标系网格组件
                    left: '15%',
                    height: '60%',
                    width: '80%'
                },
                xAxis : [
                    {  
                        splitLine:{
                            lineStyle: {
                                color: '#eee'
                            }
                        },
                        type : 'value'
                    }
                ],
                yAxis : [
                    {
                        splitLine:{show: false}, //去除网格线
                        type : 'category',
                        data : ['大连日航','北京唐拉','东莞唐拉']
                    }
                ],
                series : [
                    {
                        type:'bar',
                        data:[18203, 23489, 29034],
                        itemStyle:{
                            normal: {
                                color: '#87ADE3'
                            }
                        },
                        barCategoryGap: '70%' // 类目间柱形距离，默认为类目间距的20%，可设固定值。值越大，bar越细
                    }
                ]
            };
            // 使用刚指定的配置项和数据显示图表。
            todayTop3Chart.setOption(todayTop3Option);
        })
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

</style>
