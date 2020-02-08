<template>
  <div id="app">
    <b-container class="bv-example-row bv-example-row-flex-cols">
      <b-row>
        <b-col align-self="start">
          <Fatorial />
        </b-col>
      </b-row>
      <b-row>
        <b-col align-self="center">
          <Quadrado />
        </b-col>
        <b-col align-self="center">
          <Cubo />
        </b-col>
        <b-col align-self="center">
          <RaizQ />
        </b-col>
        <b-col align-self="end">
          <RaizC />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Fatorial from "./components/Fatorial.vue";
import Quadrado from "./components/Quadrado.vue";
import Cubo from "./components/Cubo.vue";
import RaizQ from "./components/RaizQ.vue";
import RaizC from "./components/RaizC.vue";

export default {
  name: "app",
  components: {
    Fatorial,
    Quadrado,
    Cubo,
    RaizQ,
    RaizC
  },
  methods: {},
  data() {
    return {};
  }
};
</script>

<style>
#app {
}
#container {
  margin: 10px;
}
</style>
