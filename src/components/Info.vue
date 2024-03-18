<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p>Utilizo as seguintes tecnologias para back-end:</p>
  <ul>
    <li v-for="(tec, index) in tec_back_end" v-bind:key="index">{{ tec }}</li>
  </ul>
  <p>Utilizo as seguintes tecnologias para front-end:</p>
  <ul>
    <li v-for="tec in tec_front_end" v-bind:key="tec.id">{{ tec.language }}</li>
  </ul>
  <div>
    <button @click="showEmail">{{ texto_botao }}</button>
  </div>
  <p v-show="meu_email">Mande uma mensagem para: {{ finalEmail }}</p>
  <p>Para acessar meu portfólio: <a :href="meu_link">clique aqui</a></p>
  <Picture />
</template>

<script>
import Picture from './Picture.vue'

export default {
  name: 'Info',
  components: {
    Picture
  },
  props: {
    finalEmail: String,
    esta_trabalhando: Boolean
  },
  data() {
    return {
      meu_email: false,
      meu_link: 'https://www.google.com',
      texto_botao: 'Mostrar e-mail',
      tec_back_end: ['Java', 'Node', 'Spring', 'TypeScript'],
      tec_front_end: [
        { id: 1, language: 'JavaScript' },
        { id: 2, language: 'Java - JSF' },
        { id: 3, language: 'Angular' }
      ]
    }
  },
  methods: {
    showEmail() {
      this.meu_email = !this.meu_email
      this.texto_botao = this.meu_email ? 'Esconder e-mail' : 'Mostrar e-mail'
    }
  }
}
</script>
