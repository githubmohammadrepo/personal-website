<template>
  <div>
      <hr>
      <h2>{{city}}</h2>
        <label for="city">city:</label>
        <input type="text" id="city" v-model="city" name="city">
        <input type="submit" @click="getInfo" value="submit">
  </div>
</template>

<script>
export default {
  name: "Animation",
  props: {},
  data: function() {
    return {
      show: true,
      city:'marivan'
    };
  },
  methods: {
    getInfo: function(){
      alert('hi')
       // GET /someUrl
      this.$http.get('https://jsonplaceholder.typicode.com/users/1/albums').then(response => {

        // get body data
        console.log(response);

      }, response => {
        // error callback
        console.log(response)
      });
    }
  }
};
</script>
<style  scoped>
.left{
  float: left;
  
}
.right{
  float: right;
}

</style>