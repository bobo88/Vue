<!--
内容：公共左侧栏
作者：BOBO
日期： 20170728
-->
<template>
  <div class="left-cont-wrap">
    <ul class="left-cont">
      <!-- 将"激活时的CSS类名"应用在外层元素 li  -->
      <router-link tag="li" v-for="(data, index) in linkData" :to="data.url">
        <dl>
          <dt><router-link :to="data.url">{{ data.sort }}</router-link></dt>
          <dd v-if="data.sortChild" v-for="(item, key, index) in data.sortChild">
            <router-link :to="item.url">{{ item.tit }}</router-link>
          </dd>
        </dl>
      </router-link>

    </ul>
  </div>
</template>

<script>
export default {
  name: 'left',
  data () {
    return {
      linkData: [
        {
          "sort": "财务首页", 
          "url": "/financial-index"
        },
        {
          "sort": "日报",
          "url": "/daily",
          "sortChild": [
            {"tit": "集团日报", "url": "/daily/group-daily"},
            {"tit": "酒店日报", "url": "/daily/hotel-daily"},
            {"tit": "日收入酒店对比", "url": "/daily/daily-income-hotel-comparison"},
            {"tit": "日指标明细", "url": "/daily/daily-target-breakdown"}
          ]
        },
        {"sort": "周报","url": "/weekly"},
        {"sort": "月报","url": "/monthly"}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.left-cont-wrap{ position: absolute; z-index: 2; top: 0; left: 0; padding-top: 90px; padding-right: 10px; width: 250px; height: 100%; min-height: 100vh; color: #000;
	.left-cont{ position: relative; z-index: 1; padding-top: 20px; width: 240px; height: 100%; color: #999; font-size: 16px;
    li{
      &.router-link-active{
        dd{ display: block;}
      }
      a{ display: block; padding-left: 25px; border-left: 2px solid #fff; height: 50px; line-height: 50px; color: #999;
        &.router-link-active{ color: #41A0D8;}
      }
      dl{
        dt{
          a.router-link-active{ color: #333; border-left: 2px solid #82BED9; background: rgba(130,190,217,.15);}
        }
        dd{ display: none;
          a{ padding-left: 35px;}
        }
      }
    }
	}
}
</style>
