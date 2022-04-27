<template>
  <div>
    
    <p v-if="mostra_mensagem">Estou trabalhando no momento.</p>
    <p v-else>Não estou trabalhando no momento.</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
      <li v-for="tecnologia in tecnologias" :key="tecnologia.id">{{tecnologia.linguagem}}</li>
      
    </ul>
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostra_email">Mande uma mensagem para: {{ email }}</p>
    <p>
      Para acessar meu portifólio
      <a v-bind:href="meu_link" target="_blank"> clique aqui</a>
    </p>
    <Picture />
    <Form />
  </div>
</template>
<script>
import Picture from "./Picture.vue"
import Form from "./Form.vue"

export default {
  name: "Info",
  components: {
      Picture,
      Form
  },
  props: {
    email: String
  },
  data() {
      return {
          mostra_mensagem: false,
          mostra_email: false,
          meu_link: 'https://www.google.com.br/',
          textoBotao: 'Mostrar e-mail',
          tecnologias: [
              {id: 1, linguagem:'HTML'},
              {id: 2, linguagem:'CSS'},
              {id: 3, linguagem:'Javascript'}
          ]     
      }
  },
  methods: {
      showEmail() {
          this.mostra_email = !this.mostra_email
          if(!this.mostra_email) {
            this.textoBotao = 'Mostra e-mail'
          } else {
            this.textoBotao = 'Ocultar e-mail'
          }
      }
  }
}
</script>
