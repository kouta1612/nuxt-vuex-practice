<template>
  <div>
    <p>{{ counter }}</p>
    <button @click="countUp">+1</button>
    <button @click="countDown">-1</button>
  </div>
</template>

<script>
export default {
  computed: {
    counter () {
      return this.$store.state.counter
    }
  },
  methods: {
    countUp () {
      this.$store.commit('increment')
    },
    countDown () {
      this.$store.commit('decrement')
    }
  }
}
</script>
