<!--
内容：酒店指标明细 组件
作者：BOBO
日期： 20170730
-->
<template>
	<div class="hotel-index-details" id="hotelIndexDetails">
		<h4 class="income-source-tit clearfix">酒店指标明细 <a href="#" class="fr">查看其他指标</a></h4>

        <div class="income-source-cont">
            <table cellpadding="0" cellspacing="0">
                <thead>
                    <tr>
                        <th rowspan="2">指标分类</th>
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
                        <td class="left-tit" rowspan="11">生产经营指标</td>
                        <td class="left-tit">实际出租房间数</td>
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
                        <td class="left-tit">可供出租房间数</td>
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
                        <td class="left-tit">其中：长期自用房</td>
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
                        <td class="left-tit">临时自用房</td>
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
                        <td class="left-tit">免费房</td>
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
                        <td class="left-tit">坏房数</td>
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
                        <td class="left-tit">总入住人数</td>
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
                        <td class="left-tit">入住率</td>
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
                        <td class="left-tit">平均房价</td>
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
                        <td class="left-tit">餐饮消费人数</td>
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
                        <td class="left-tit">餐饮人均消费</td>
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
</template>

<script>
export default {
	name: 'hotel-index-details',
	data () {
		return {
		  	msg: ''
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.income-source-tit{ margin-bottom: 10px; height: 25px; line-height: 25px; font-size: 14px; color: #344559; letter-spacing: 1px;
    a{ font-size: 12px; color: #4A90E2; letter-spacing: 0.86px;}
}
.tc{ text-align: center;}
.income-source-cont{ width: 100%; height: 450px; overflow: auto;
    table{ width: 100%; border: 1px solid #eee;
        thead{ background: #f9f9f9;
            tr{ line-height: 30px;}
            th{ padding: 0 10px; border-right: 1px solid #eee; border-bottom: 1px solid #eee; text-align: center;}
        }
        tr{ line-height: 36px; border-bottom: 1px solid #eee;
            td{ padding: 0 10px; min-width: 80px; border-right: 1px solid #eee; border-bottom: 1px solid #eee; text-align: center;}
            .left-tit{ min-width: 140px;}
        }
    }
}
</style>
