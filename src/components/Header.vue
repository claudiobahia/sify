<template>
  <div>
    <h1>Header</h1>
    <p>Vem direto do App.vue {{ horas }}</p>
  </div>
</template>

<script>
export default {
  props: ["horas"]
};
</script>

<style>
</style>