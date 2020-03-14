<template>
  <div id="app">
    <div class="vh-100">
      <VueNav />
      <hr width="0px" class="my-2">
      <div class="flex-column justify-content-center">
        <Carosel />
      </div>
    </div>
  </div>
</template>

<script>
import VueNav from './components/vue-navbar'
import Carosel from './components/Carosel'

export default {
  name: 'App',
  components: {
    VueNav,
    Carosel
  }
}
</script>

<style lang="scss">

#app {
  .vh-100{
    height: 100%vh;
  }
}
</style>
