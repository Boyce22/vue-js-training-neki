<template>
  <h1>Meu nome é {{ nome }}</h1>
</template>

<script>
export default {
  name: 'LifeCycle',
  data() {
    return {
      nome: 'Ainda não sei'
    }
  },
  created() {
    setTimeout(() => {
      this.nome = 'Bernardo'
    }, 1000)
  },
  mounted() {
    setTimeout(() => {
      this.nome = 'Boyce'
    }, 1200)
  }
}
</script>
