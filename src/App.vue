<template>
  <div id="app">
    <img src="./assets/logo.png">
    <p>Title: {{ movieTitle }}</p>
    <p>Released: {{ movieReleaseDate }}</p>
    <p>The movie is {{ oldOrNew(movieReleaseDate) ? 'old' : 'new' }}.</p>
    <div v-bind:title="movieTitle">Hover your mouse here</div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      movieTitle: 'War Games',
      movieReleaseDate: 1983
    }
  },
  methods: {
    oldOrNew: function(movieReleaseDate) {
      return movieReleaseDate < 2000;
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

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
