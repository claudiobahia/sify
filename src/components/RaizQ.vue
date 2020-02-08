<template>
  <div>
    <b-jumbotron id="container">
      <h1>Raiz quadrada</h1>
      <b-input-group prepend="Número" class="mt-3">
        <b-form-input type="number" v-model="inp_raizq"></b-form-input>
        <b-button variant="primary" v-on:click="raizq()">Calcular</b-button>
      </b-input-group>
      <p>{{ x_raizq }}</p>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  methods: {
    raizq: function() {
      let inp_raizq = this.inp_raizq;
      this.x_raizq = `Resultado: ${inp_raizq ** (1 / 2)}`;
    }
  },
  data() {
    return {
      x_raizq: "Resultado: "
    };
  }
};
</script>

<style>
</style>