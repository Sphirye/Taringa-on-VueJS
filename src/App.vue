<template>
  <div id="app">
    <div>
      <fixedInterface/>
      <feed/>
    </div>
  </div>
</template>

<style>

*{ 
  margin: 0px;
}

#page {
    height: 100%; width: 100%
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>

<script>
import fixedInterface from './components/fixedInterface.vue';
import feed from './components/feed.vue';

export default {
  components: {
    fixedInterface,
    feed
  }
}
</script>