<!--
内容：公共左侧栏
作者：BOBO
日期： 20170728
-->
<template>
  <div class="left-cont-wrap">
    <ul class="left-cont">
      <li>
        <dl>
          <dt><a href="javascript:;">财务首页</a></dt>
        </dl>
      </li>
      <li>
        <dl>
          <dt class="current"><a href="javascript:;">日报</a></dt>
          <dd><a href="javascript:;" class="on">集团日报</a></dd>
          <dd><a href="javascript:;">酒店日报</a></dd>
          <dd><a href="javascript:;">日收入酒店对比</a></dd>
          <dd><a href="javascript:;">日指标明细</a></dd>
        </dl>
      </li>
      <li>
        <dl>
          <dt><a href="javascript:;">周报</a></dt>
        </dl>
      </li>
      <li>
        <dl>
          <dt><a href="javascript:;">月报</a></dt>
        </dl>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'left',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.left-cont-wrap{ position: absolute; z-index: 2; top: 0; left: 0; padding-top: 90px; padding-right: 10px; width: 250px; height: 100%; min-height: 100vh; color: #000;
	.left-cont{ position: relative; z-index: 1; padding-top: 20px; width: 240px; height: 100%; color: #999; font-size: 16px;
    li{
      a{ height: 50px; line-height: 50px; color: #999;
        &.on{ color: #41A0D8;}
      }
      dl{
        dt{ padding-left: 25px; border-left: 2px solid #fff;
          &.current{ border-left: 2px solid #82BED9; background: rgba(130,190,217,.15);
            a{ color: #333;}
          }
        }
        dd{ padding-left: 35px;}
      }
    }
	}
}
</style>
