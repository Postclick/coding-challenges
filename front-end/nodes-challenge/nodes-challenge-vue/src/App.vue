<template>
  <div id="App">
    <NodeArena/>
  </div>
</template>

<script>
import NodeArena from './components/NodeArena.vue'

export default {
  name: 'App',
  components: {
    NodeArena
  }
}
</script>

<style>
#App {
    font-family: sans-serif;
    text-align: center;
}

body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
        "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
        sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

code {
    font-family: source-code-pro, Menlo, Monaco, Consolas, "Courier New", monospace;
}
</style>
