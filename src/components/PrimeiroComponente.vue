<template>
    <div> 
    <h1>Olá Vue!</h1>
    <p>O meu nome é {{nome}}, e meu sobrenome é {{ Sobrenome }}!</p>
    </div>
</template>

<script>
    export default {
        name: 'PrimeiroComponente',
        data() {
            return{
                nome: 'Felipe',
                Sobrenome: 'Gomes'
            }
        }
    }

</script>
