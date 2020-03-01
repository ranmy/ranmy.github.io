<template>
  <div id="app" style="margin: 0px">
    <div>
      <TopHead/>
    </div>
    <div style="margin-top: 10px">
      <TimeLine/>
    </div>
  </div>
</template>

<script>
import TimeLine from './components/TimeLine.vue'
import TopHead from './components/TopHead.vue'
export default {
  name: 'App',
  components: {
    TimeLine,
    TopHead
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0px;
  padding: 0px;
}


</style>
