<template>
  <div>
    <button @click="primeiro($event), segundo($event)">Ativar multiplos eventos:</button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: 'MultiplosEventos',
  data() {
    return {
      multiplos_eventos: ''
    }
  },
  methods: {
    primeiro(e) {
      this.multiplos_eventos = 'Primeiro evento ativado'
    },
    segundo(e) {
      setTimeout(() => {
        this.multiplos_eventos = 'Segundo evento ativado'
      }, 1000)
    }
  }
}
</script>
