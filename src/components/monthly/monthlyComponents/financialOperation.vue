<!--
内容：月报 ~ 财务运营KPI
作者：BOBO
日期： 20170731
-->
<template>
  <div class="financial-operation" id="financialOperation">
  	财务运营KPI
  </div>
</template>

<script>
import echarts from 'echarts'

export default {
  name: 'financial-operation',
  data () {
    return {
      msg: ''
    }
  },
  mounted(){
		this.$nextTick(function() {
            var todayTop3Chart = echarts.init(document.getElementById('financialOperation'));
            var todayTop3Option = {
                title: {
                    text: '财务运营KPI',
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
                    	splitLine:{show: false}, //去除网格线
                    	type : 'category',
                    	data : ['经营收入','经营费用','经营毛利', '非经营费用', '利润总额', '净利润']
                        
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
                        type:'bar',
                        data:[56789, 23489, 29034, 12344, 45633, 16789],
                        itemStyle:{
                            normal: {
                                color: function(params) {
                                	var colorList = ['#48cda6','#fd87ab','#11abff', '#006699', '#ff6600', '#b3c8e8'];
                                	return colorList[params.dataIndex];
                                }
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