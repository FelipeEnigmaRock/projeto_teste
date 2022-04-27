<template>
  <div>
    <h2>Meu Formulario</h2>
    <form action="" @submit="enviarFormulario">
      <input type="text" v-model="name" /> <br />
      <input type="text" v-model="email" /> <br />
      <input type="submit" />
    </form>
  </div>
</template>

<script>
export default {
    name: 'Form',
    data() {
        return {
            name: "",
            email: ""
        }
    },
    methods: {
        enviarFormulario(e) {
            e.preventDefault();

            const name = this.name;
            const email = this.email;

        console.log('enviado: ' + name)
        }
    }
}
</script>
