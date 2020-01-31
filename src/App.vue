<template>
  <div id="app">
    <Header v-bind:horas="horass" />
    <p v-if="horass < 12">Está de dia</p>
    <input id="inp" type="number" v-model="n" />
    <button v-on:click="fatorial()">Calcular fatorial</button>
    <p>{{ x }}</p>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    Footer
  },
  methods: {
    fatorial: function() {
      let n = this.n;
      for (let i = n - 1; i != 0; i--) {
        n = n * i;
      }
      this.x = `Resultado: ${n}`;
    }
  },
  data() {
    return {
      n: 0,
      x: "",
      horass: new Date().getHours()
    };
  }
};
</script>

<style>
#app {
  text-align: center
}
</style>
