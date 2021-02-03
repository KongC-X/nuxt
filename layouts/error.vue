<template>
  <div>
    <h1>对不起，出错啦！</h1>
    <!-- {{error}} -->
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'error_layout' // 不指定错误页面布局的话，则会使用default默认布局
}
</script>

<style>

</style>
