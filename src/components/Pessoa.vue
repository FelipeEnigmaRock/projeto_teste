<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info :email= "email"/>
  </div>
</template>

<script>
import Info from './Info.vue';

export default {
      name: 'Pessoa',
      components: {
          Info
      },
     data() {
        return {
            nome: 'Felipe',
            email: "orochimaru@gmail.com"
            
        };
    }
}
</script>
