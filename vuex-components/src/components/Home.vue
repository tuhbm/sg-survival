<template>
  <div class="container">
    <div class="row text-center">
      <h3>Clicked: {{ $store.state.count }} times, counter is {{ evenOrOdd }}</h3>
      <button class="btn btn-success" @click="increment">+</button>
      <button class="btn btn-danger" @click="decrement">-</button>

      <button class="btn btn-default" @click="incrementIfOdd">Increment if odd</button>
      <button class="btn btn-default" @click="incrementAsync">Increment async</button>
    </div>
  </div>
</template>

<script>
  import {mapGetters, mapActions} from 'vuex'

  export default {
    name: 'HelloWorld',
    methods: {
      ...mapActions([
        'increment',
        'decrement',
        'incrementIfOdd',
        'incrementAsync'
      ])
    },
    computed: {
      ...mapGetters([
        'evenOrOdd'
      ])
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
