<!--
内容：公共头部
作者：BOBO
日期： 20170728
-->
<template>
	<div class="top">
		<div class="tit-cont-wrap">
			<span class="logo"><img src="http://www.yuanbo88.com/dist/images/styleimg/logo2.png" alt=""></span>
			<ul class="nav-list clearfix">
				<li><a href="javascript:;">管理驾驶舱</a></li>
				<li class="on"><a href="javascript:;">财务</a></li>
				<li><a href="javascript:;">运营</a></li>
				<li><a href="javascript:;">市场</a></li>
				<li><a href="javascript:;">品牌</a></li>
				<li><a href="javascript:;">投资</a></li>
				<li><a href="javascript:;">创新</a></li>
			</ul>
		</div>

		<!-- <h3 class="tit-cont-wrap"><span>我是头部内容</span></h3> -->
	</div>
</template>

<script>
export default {
  name: 'top',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.tit-cont-wrap{ position: absolute; z-index: 3; top: 0; left: 0; width: 100%; height: 90px; line-height: 90px; color: #fff; font-size: 24px; background: #46576B;
	.logo{ position: absolute; z-index: 4; top: 15px; left: 40px; width: 170px; height: 60px;}
	.nav-list{ width: 100%; padding-left: 250px; height: 90px;
		li{ float: left; display: inline-block; margin-right: 10px;
			&:hover, &.on{
				a{ background: rgba(0,0,0,.2); border-radius: 20px;}
			}
			a{ padding: 10px 30px; height: 20px; line-height: 20px; color: #fff; font-size: 16px;}
		}
	}
}
</style>
