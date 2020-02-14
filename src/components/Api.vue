<template>
  <div id="api">
    <h1>API IMDB</h1>
    {{info}}
  </div>
</template>

<script>
import axios from "axios";

export default {
  mounted() {
    axios
      .get("https://api.github.com/users/claudiobahia")
      .then(response => (this.info = response));
  },
  methods: {},
  data() {
    return {
      info: null
    };
  }
};
</script>

<style>
</style>