<template>
  <div id="app">
    <div class="vh-100 d-flex justify-content-center flex-wrap">
      <VueNav class="w-100"/>
      <!-- <hr width="0px" class="my-2"> -->
        <div class="w-100"></div>
        <Carosel class=" w-75 m-auto"/>
        <div class="w-100"></div>
        <div class="w-100"></div>

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
