<template>
  <div id="app">
    <home/>
  </div>
</template>

<script>
import Home from "./views/home/home"
export default {
  name: 'App',
  components: {
    Home,
  },
}
</script>

<style>
  @import "./assets/css/base.css"
</style>
