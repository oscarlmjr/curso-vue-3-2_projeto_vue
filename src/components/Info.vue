<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Utilizo as seguintes tecnologias:</p>
  <ul>
    <li>JavaScript</li>
    <li>PHP</li>
    <li>Python</li>
  </ul>  
    <button @click="showEmail">{{ textoBotao }}</button>
  <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
  <p>Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
  <Picture />
  <p v-if="4 > 2">Testando</p>
</div>  
</template>
<script>
import Picture from './Picture'

export default {
  name: 'Info',
  components: {
      Picture
      },
    data() {
      return { 
        esta_trabalhando: false,
        mostrar_email: false,
        email: 'matheus@email.com',
        meu_link: "https://www.google.com",
        textoBotao: 'Mostrar e-mail'
      }
    },
    methods: {
      showEmail() {
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email) {
          this.textoBotao = 'Mostrar e-mail'
        } else {
          this.textoBotao = 'Esconder e-mail'
        }
      }
    }
  }
</script>