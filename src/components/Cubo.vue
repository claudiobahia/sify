<template>
  <div>
    <b-jumbotron id="container">
      <h1>Cubo</h1>
      <b-input-group prepend="Número" class="mt-3">
        <b-form-input type="number" v-model="inp_cubo"></b-form-input>
        <b-button variant="primary" v-on:click="cubo()">Calcular</b-button>
      </b-input-group>
      <p>{{ x_cubo }}</p>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  methods: {
    cubo: function() {
      let inp_cubo = this.inp_cubo;
      this.x_cubo = `Resultado: ${inp_cubo ** 3}`;
    }
  },
  data() {
    return {
      x_cubo: "Resultado: "
    };
  }
};
</script>

<style>
</style>