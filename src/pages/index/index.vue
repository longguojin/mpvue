<template>
  <div class="container">
    <p class="count">Vuex counter：{{ count }}</p>

    <p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </p>
  </div>
</template>

<script>
// Use Vuex
import store from './store'

export default {
  computed: {
    count () {
      return store.state.count
    }
  },
  methods: {
    increment () {
      store.commit('increment')
      this.ct++
    },
    decrement () {
      store.commit('decrement')
    }
  }
}
</script>

<style lang="scss" scoped>
.container{
  .count{
    font-size: 26px;
  }
}
</style>

