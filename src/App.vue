<template>
  <div id="app">
    <div class="vh-100 d-flex justify-content-center flex-wrap">
      <VueNav class="w-100" />
      <!-- <hr width="0px" class="my-2"> -->

      <b-alert class="w-100 text-center bg-warning" show dismissible>
          <h5>سلام به وبسایت من خوش اومدید</h5>
          <p>من قصد دارم بهترین سایت ممکن رو برای شما عزیزان طراحی و کد نویسی بکنم</p>
        </b-alert>

      <div class="w-100 row">
        <Carosel class="col-sm-12 col-lg-9 m-auto px-2" />
        <Aside class="col-sm-12 col-lg-3 m-auto float-right" />
      </div>
      <div class="w-100"></div>
      <div class="w-100"></div>
    </div>
  </div>
</template>

<script>
import VueNav from "./components/vue-navbar";
import Carosel from "./components/Carosel";
import Aside from "./components/Aside";

export default {
  name: "App",
  components: {
    VueNav,
    Carosel,
    Aside
  }
};
</script>

<style lang="scss">
#app {
  .vh-100 {
    height: 100%vh;
  }
}
</style>
