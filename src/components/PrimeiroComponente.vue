<template>
  <h1>Olá mundo</h1>
  <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
  <MultiplosEventos />
  <Reutilizacao />
  <Reutilizacao />
  <Reutilizacao />
  <Reutilizacao />
  <Reutilizacao />
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'
export default {
  name: 'PrimeiroComponente',
  data() {
    return {
      nome: 'Bernardo',
      profissao: 'Desenvolvedor full-stack'
    }
  },
  components: {
    MultiplosEventos,
    Reutilizacao
  }
}
</script>
