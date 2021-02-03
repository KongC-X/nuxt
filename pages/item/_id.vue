<template>
  <div>
    <h1>商品</h1>
    <br>
    <hr>
    <br>
    <div v-if="this.$route.params.id">
      商品ID : {{ this.$route.params.id }}
    </div>
  </div>
</template>

<script>
export default {
  validate ({ params }) {
    return /^\d+$/.test(params.id)
  }
}
</script>

<style>

</style>
