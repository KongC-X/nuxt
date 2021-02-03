<template>
  <div>
    <h1>商品详细</h1>
    <hr>
    <div v-if="this.$route.params.name">
      标签名：{{ this.$route.params.tag }} / {{ this.$route.params.name }}
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
