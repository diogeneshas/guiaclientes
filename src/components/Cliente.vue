<template>
    <div v-bind:class="{'cliente': !isPremium, 'cliente-premium': isPremium}">
        <h4>Nome: {{nome}}</h4>
        <hr>
        <p>{{descricao}}</p>
        <hr>
        <p>Email: {{email}}</p>
        <p v-if="showIdade === true">Idade: {{idade}}</p>
        <p v-else>O usuario escondeu a idade!</p>
    </div>
</template>


<script>
export default {
    data(){
        return{
            numero: '2323',
            email: 'diogenes@gmail.com',
            descricao: 'Lorem ipsum Lorem ipsum',
            isPremium: false
        }
    },
    props: {
        nome: String,
        idade: Number,
        showIdade: Boolean
    }
}
</script>


<style scoped>
    .cliente {
        background-color: #ECE5E3;
        max-width: 600px;
        height: 230px;
        padding: 1%;
        margin-bottom: 10px;
    }
    .cliente-premium {
        background-color: black;
        color: yellow;
        max-width: 600px;
        height: 230px;
        padding: 1%;
        margin-bottom: 10px;
    }
</style>