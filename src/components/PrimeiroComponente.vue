<template>
    <div> 
    <h1>Olá Vue!</h1>
    <p>O meu nome é {{nome}}, e meu sobrenome é {{ Sobrenome }}!</p>
    <MultiplosEventos />
    </div>
</template>

<script>
    import MultiplosEventos from "./MultiplosEventos.vue"

    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos
        },
        data() {
            return{
                nome: 'Felipe',
                Sobrenome: 'Gomes'
            }
        }
    }

</script>
