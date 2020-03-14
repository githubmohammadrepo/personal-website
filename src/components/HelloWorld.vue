<template>
  <div class="hello">
    <button v-on:click="show = !show" class="btn btn-info">Toogle</button>

    <transition name="fade">
      <h1 v-if="show">{{ msg }}</h1>
    </transition>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: function() {
    return {
      show: true
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

button {
  padding: 8px 12px;
  border-radius: 6px;
  font-size: 1.2rem;
  background-color: crimson;
  color: white;
}
button:hover {
  background: brown;
}




/* css transitiono in vuejs  */
.fade-enter /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  color:gold;
}

.fade-enter-to /* .fade-leave-active below version 2.1.8 */ {
  transition: opacity .5s;
  color:blue;
  opacity: 1;
}
.fade-enter-active{
  transition: opacity .5s;
  color:red;
}



.fade-leave-active {
  color:coral;
  transition: opacity .5s;
}

.fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  color:darkgreen;
}
</style>
