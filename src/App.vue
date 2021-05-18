<template>
  <div id="app">
    <h1>Guia Clientes</h1>
    <Cliente v-bind:nome="nomeDoDiogenes" idade="36" v-bind:showIdade="true" />
    <Cliente nome="henrique" idade='16' v-bind:showIdade="false"/>
    <Cliente nome="almeida" idade='37' v-bind:showIdade="true"/>
    <div v-for="(cliente,index) in clientes" v-bind:key="cliente.id">
      <p>{{index}}</p>
      {{cliente}}
    </div>
  </div>
</template>

<script>

import Cliente from './components/Cliente'

export default {
  name: 'App',
  data() {
    return{
      nomeDoDiogenes: "Diogenes henrique de Almeida Silva",
      clientes: [{
        id: 1,
        nome: 'diogenes',
        email: 'diogenes@gmail.com',
        idade: 36
      },
      {
        id: 2,
        nome: 'henrique',
        email: 'henrique@gmail.com',
        idade: 16
      },
      {
        id: 3,
        nome: 'almeida',
        email: 'almeida@gmail.com',
        idade: 37
      }]
    }
  },
  components: {
    Cliente
  }
}
</script>

<style>
</style>
