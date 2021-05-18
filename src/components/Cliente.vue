<template>
    <div id="cliente">
        <input type="text" v-bind:value="nome">
        <hr>
        <input type="text" v-bind:value="descricao">
        <h2 id="cliente-nome">{{nome}}</h2>
        <p>Descrição do cliente: {{descricao}}</p>
    </div>
</template>


<script>
export default {
    data(){
        return{
            nome: 'diogenes',
            numero: '',
            email: '',
            idade: 0,
            descricao: 'Lorem ipsum Lorem ipsum'
        }
    }
}
</script>


<style scoped>
    #cliente {
        color: blue;
        background-color: black;
        max-width: 600px;
    }
    #cliente-nome {
        color: white;
    }
</style>