<template>
  <b-list-group class="list-items pr-0">
    <b-list-group-item disabled class="text-center">نوع پروژه های انجام شده</b-list-group-item>
    <b-list-group-item class="d-flex justify-content-between align-items-center">
      <b-link href="#foo">Html</b-link>
      <b-badge variant="primary" pill>14</b-badge>
    </b-list-group-item>
    <b-list-group-item class="d-flex justify-content-between align-items-center">
      <b-link href="#foo">Css</b-link>
      <b-badge variant="primary" pill>2</b-badge>
    </b-list-group-item>
    <b-list-group-item class="d-flex justify-content-between align-items-center">
      <b-link href="#foo">Javascript</b-link>
      <b-badge variant="primary" pill>1</b-badge>
    </b-list-group-item>
    <b-list-group-item class="d-flex justify-content-between align-items-center">
      <b-link href="#foo">Bootstrap</b-link>
      <b-badge variant="primary" pill>14</b-badge>
    </b-list-group-item>

    <b-list-group-item class="d-flex justify-content-between align-items-center">
      <b-link href="#foo">php</b-link>
      <b-badge variant="primary" pill>2</b-badge>
    </b-list-group-item>

    <b-list-group-item class="d-flex justify-content-between align-items-center">
      <b-link href="#foo">Vuejs</b-link>
      <b-badge variant="primary" pill>1</b-badge>
    </b-list-group-item>

    <b-list-group-item class="d-flex justify-content-between align-items-center">
      <b-link href="#foo">Laravel</b-link>
      <b-badge variant="primary" pill>1</b-badge>
    </b-list-group-item>
  </b-list-group>
</template>

<script>
export default {
  name: "Aside",
  props: {
    msg: String
  },
  data: function() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.list-items > :hover {
  background-color: rgba(0, 173, 253, 0.685);
  color: white;
}
.list-items > :hover * {
  color: white;
  font-weight: bold;
}
</style>
