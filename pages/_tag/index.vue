<template>
  <div>
    <h1>商品一览({{ this.$route.params.tag }})</h1>
    <hr>
    <ul>
      <li><a :href="this.$route.params.tag + '/Zelda'">Zelda</a></li>
      <li><a :href="this.$route.params.tag + '/Mario'">Mario</a></li>
    </ul>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
