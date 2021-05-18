<template>
  <div id="app">
    <h1>Guia Clientes</h1>
    <Cliente v-bind:nome="nomeDoDiogenes" idade="36" v-bind:showIdade="true" />
    <Cliente nome="henrique" idade='16' v-bind:showIdade="false"/>
    <Cliente nome="almeida" idade='37' v-bind:showIdade="true"/>
  </div>
</template>

<script>

import Cliente from './components/Cliente'

export default {
  name: 'App',
  data() {
    return{
      nomeDoDiogenes: "Diogenes henrique de Almeida Silva"
    }
  },
  components: {
    Cliente
  }
}
</script>

<style>
</style>
