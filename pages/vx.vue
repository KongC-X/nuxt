<template>
  <div>
    <button @click="increment">
      喜加一
    </button>
    <div>{{ counter }}</div>
  </div>
</template>

<script>
import { mapState, mapMutations } from 'vuex'

export default {
  name: 'Vx',
  components: {
    // HelloWorld
  },
  props: {},
  data () {
    return {}
  },
  computed: {
    // 映射store.state
    ...mapState({
      counter: state => state.counter
    })
  },
  methods: {
    // 映射store.mutations
    ...mapMutations({
      increment: 'increment'
    })
  }
}
</script>

<style>

</style>
