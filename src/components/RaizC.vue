<template>
  <div>
    <b-jumbotron id="container">
      <h1>Raiz cúbica</h1>
      <b-input-group prepend="Número" class="mt-3">
        <b-form-input type="number" v-model="inp_raizq"></b-form-input>
        <b-button variant="primary" v-on:click="raizc()">Calcular</b-button>
      </b-input-group>
      <p>{{ x_raizc }}</p>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  methods: {
    raizc: function() {
      let inp_raizc = this.inp_raizc;
      this.x_raizc = `Resultado: ${inp_raizc ** (1 / 2)}`;
    }
  },
  data() {
    return {
      x_raizc: "Resultado: "
    };
  }
};
</script>

<style>
</style>