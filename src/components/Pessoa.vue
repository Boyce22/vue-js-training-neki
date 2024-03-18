<template>
  <h2>Está é a descrição da pessoa: {{ nome }}</h2>
  <Info :finalEmail="email" :esta_trabalhando="true" />
  <Form />
</template>

<script>
import Info from './Info.vue'
import Form from './Form.vue'

export default {
  name: 'Pessoa',
  components: {
    Info,
    Form
  },
  data() {
    return {
      nome: 'Bernardo',
      email: 'boyce-pro@gmail.com'
    }
  }
}
</script>
