<template>
  <div>
    <div>
      <h1>关于</h1>
      <hr>
      <div>
        <b-button variant="success" @click="fetchGames()">
          装载服务器数据
        </b-button>
        <hr>
        <ul>
          <li v-for="item in list" :key="item.name">
            {{ item.name }} - {{ item.price }}
          </li>
        </ul>
      </div>
    </div>
    <img src="/images/2.jpg" alt="234" class="about-img">
  </div>
</template>

<script>
export default {
  data () {
    return {
      list: []
    }
  },
  methods: {
    async fetchGames () {
      const data = await this.$axios.$get('https://raw.githubusercontent.com/komavideo/LearnNuxtJS/main/games.json')
      this.list = data
    }
  }
}
</script>

<style>
.about-img{
  width: 70%;
  height: 600px;
  margin-left: 15%;
}
</style>
