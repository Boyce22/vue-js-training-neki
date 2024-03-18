<template>
  <h1>Meu formulário</h1>
  <form action="" @submit="enviarFormulario($event)">
    <div>
      <input type="text" v-model="name" />
    </div>
    <div>
      <input type="text" v-model="email" />
    </div>
    <div>
      <Submit />
    </div>
  </form>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
</template>

<script>
import Submit from '../components/Form/Submit.vue'
import InputText from '../components/Form/InputText.vue'

export default {
  name: 'Form',
  components: {
    Submit,
    InputText
  },
  data() {
    return {
      name: '',
      email: ''
    }
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault()

      const name = this.name
      const email = this.email
    }
  }
}
</script>

<style scoped>
p {
  margin: 150px;
}
</style>
