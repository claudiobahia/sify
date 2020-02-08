<template>
  <div>
    <b-jumbotron id="container">
      <h1>Fatorial</h1>
      <b-input-group prepend="Número" class="mt-3">
        <b-form-input type="number" v-model="inp_fatorial"></b-form-input>
        <b-button v-on:click="fatorial()" variant="primary">Calcular</b-button>
      </b-input-group>
      <p>{{ x_fatorial }}</p>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  methods: {
    fatorial: function() {
      let inp_fatorial = this.inp_fatorial;
      if (inp_fatorial > 0) {
        for (let i = inp_fatorial - 1; i != 0; i--) {
          inp_fatorial = inp_fatorial * i;
        }
        this.x_fatorial = `Resultado: ${inp_fatorial}`;
      } else this.x_fatorial = "Número menor que 0.";
    }
  },
  data() {
    return {
      x_fatorial: "Resultado: "
    };
  }
};
</script>

<style>
</style>