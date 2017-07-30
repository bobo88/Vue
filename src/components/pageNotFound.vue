<template>
  <div class="page-not-found">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'page-not-found',
  data () {
    return {
      msg: '模块正在开发中，敬请期待...'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1{ padding: 100px; color: #069; font-size: 30px;}
</style>
