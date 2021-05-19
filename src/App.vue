<template>
  <div id="app">
    <h3>Cadastro: </h3>
    <small id="nomeErro" v-show="deuErro">O nome é invalido, tente novamente!</small><br>
    <input type="text" placeholder="nome" v-model="nomeField"><br>
    <input type="email" placeholder="email" v-model="emailField"><br>
    <input type="number" placeholder="idade" v-model="idadeField"><br>
    <button v-on:click="cadastrarUsuario">Cadastrar</button>
    <hr>



    <h1>Guia Clientes</h1>
    <Cliente v-bind:nome="nomeDoDiogenes" idade="36" v-bind:showIdade="true" />
    <Cliente nome="henrique" idade='16' v-bind:showIdade="false" @meDelete="deletarUsuario"/>
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
      }],
      nomeField: "",
      emailField: "",
      idadeField: "",
      deuErro: false
    }
  },
  components: {
    Cliente
  },
  methods: {
    cadastrarUsuario() {
      if(this.nomeField == '' || this.nomeField == ' ' || this.nomeField.length < 3) {
        this.deuErro = true;
      } else {
        this.clientes.push({nome: this.nomeField, email: this.emailField, idade: this.idadeField, id: Date.now()})
        this.deuErro = false;
      }
    },
    deletarUsuario() {
      console.log('Recebendo evento')
    }
  }
}
</script>

<style>
  #nomeErro {
    color: red;
  }
</style>
