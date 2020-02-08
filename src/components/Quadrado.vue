<template>
  <div>
    <b-jumbotron id="container">
      <h1>Quadrado</h1>
      <b-input-group prepend="Número" class="mt-3">
        <b-form-input type="number" v-model="inp_quadrado"></b-form-input>
        <b-button variant="primary" v-on:click="quadrado()">Calcular</b-button>
      </b-input-group>
      <p>{{ x_quadrado }}</p>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  methods: {
    quadrado: function() {
      let inp_quadrado = this.inp_quadrado;
      this.x_quadrado = `Resultado: ${inp_quadrado ** 2}`;
    }
  },
  data() {
    return {
      x_quadrado: "Resultado: "
    };
  }
};
</script>

<style>
</style>