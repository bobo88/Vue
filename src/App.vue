<!--
内容：APP入口页面
作者：BOBO
日期： 20170728
-->
<template>
  <div id="app">
    <!-- 公共头部 -->
    <public-top></public-top>

    <!-- 公共左侧栏 -->
    <public-left></public-left>

    <router-view></router-view>
  </div>
</template>

<script>
import Vue from 'vue'
// 下面路径中的 @ 是webpack配置的路径别名，可参阅build/webpack.base.conf.js
import publicTop from '@/components/common/Top'
import publicLeft from '@/components/common/Left'

import axios from 'axios'
import iView from 'iview'
import 'iview/dist/styles/iview.css'    // 使用 CSS
import '@/fonts/iconfont.css'    // 使用 iconfont图标库

Vue.use(iView)

export default {
  components: {
    publicTop,
    publicLeft
  },
  name: 'app'
}
</script>

<style>
  *{ margin: 0; padding: 0; box-sizing: border-box;}
  caption,th{text-align:left;}
  h1,h2,h3,h4,h5,h6{font-size:100%;font-weight:normal;}
  .clearfix:after{content:".";display:block;height:0;clear:both;visibility:hidden;}
  .clearfix{display:inline-block;}
  * html .clearfix{height:1%;}
  .clearfix{display:block;}
  .fl{ float: left;}
  .fr{ float: right;}
  .f12{ font-size: 12px;}

  /* 图标样式 */
  .icon-up{ color: #37BD4B; font-weight: bold;}
  .icon-yuandian{ color: #37BD4B; font-weight: bold;}
  .icon-down{ color: #eb6751; font-weight: bold;}

  .color-orange{ color: #eb6751;}

  #app {
    position: relative; z-index: 1; width: 100%; min-width: 1200px; height: 100%; min-height: 100vh; padding-top: 100px; padding-left: 260px;
    font-family: "微软雅黑",Helvetica,Arial,"Hiragino Sans GB","Microsoft YaHei",STHeiti,"华文细黑",sans-serif;
    color: #2c3e50;
  }
</style>
