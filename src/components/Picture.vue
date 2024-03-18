<template>
  <img :src="avatar" :alt="descricao" height="300px" width="300px" />
  <MudarImagem @mudar-imagem="mudarImagem" />
</template>

<script>
import MudarImagem from './MudarImagem.vue'

export default {
  name: 'Picture',
  data() {
    return {
      avatar: 'https://i.pinimg.com/originals/87/34/44/8734447f865c033c6310142c369eaf4b.jpg',
      descricao: 'Bernardo Alves'
    }
  },
  methods: {
    mudarImagem() {
      this.avatar =
        'https://img.freepik.com/fotos-premium/um-gato-roxo-peludo-com-fundo-roxo_1043462-3.jpg'
    }
  },
  components: {
    MudarImagem
  }
}
</script>
