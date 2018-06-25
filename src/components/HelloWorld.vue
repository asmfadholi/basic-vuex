<template>
<div class="container">
  <div class="text-center">
    <h3>Clicked: {{ $store.state.count }} times, counter is {{ evenOrOdd }}</h3>

    <button class="btn btn-success" @click='increment'> + </button>
    <button class="btn btn-danger" @click='decrement'> - </button>

    <button class="btn" @click='incrementIfOdd'> increment If Odd </button>
    <button class="btn" @click='incrementAsync'> increment Async </button>
  </div>

</div>
</template>

<script>
import {
  mapGetters,
  mapActions
} from 'vuex'

export default {
  name: 'hello',
  computed: mapGetters([
    'evenOrOdd'
  ]),
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
  ]),
  data() {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
