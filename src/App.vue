<template>
  <div id="app">
    <tweets-page />
  </div>
</template>

<script>
import TweetsPage from './components/tweets.vue';

export default {
  name: 'App',
  components: {
    TweetsPage
  }
}
</script>

<style>
#app {
  font-family: 'Roboto Mono', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
