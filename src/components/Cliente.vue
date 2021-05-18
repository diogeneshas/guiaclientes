<template>
    <div id="cliente">
        <h4>Nome: {{nome}}</h4>
        <hr>
        <p>{{descricao}}</p>
        <hr>
        <p>Email: {{email}}</p>
        <p>Idade: {{idade}}</p>
    </div>
</template>


<script>
export default {
    data(){
        return{
            numero: '2323',
            email: 'diogenes@gmail.com',
            descricao: 'Lorem ipsum Lorem ipsum'
        }
    },
    props: {
        nome: String,
        idade: Number,
        cliente: Object
    }
}
</script>


<style scoped>
    #cliente {
        background-color: #ECE5E3;
        max-width: 600px;
        height: 230px;
        padding: 1%;
        margin-bottom: 10px;
    }
</style>