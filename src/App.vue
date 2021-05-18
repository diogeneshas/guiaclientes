<template>
  <div id="app">
    <h1>Guia Clientes</h1>
    <Cliente v-bind:nome="nomeDoDiogenes" />
    <Cliente nome="henrique" idade='16'/>
    <cliente v-bind:cliente="clienteHenrique" />
  </div>
</template>

<script>

import Cliente from './components/Cliente'

export default {
  name: 'App',
  data() {
    return{
      nomeDoDiogenes: "Diogenes henrique de Almeida Silva",
      clienteHenrique: {
        nome: 'henrique',
        idade: '16'
      }
    }
  },
  components: {
    Cliente
  }
}
</script>

<style>
</style>
