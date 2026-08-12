<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Utilizo as seguintes tecnologia para back-end:</p>
    <ul>
      <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
        <!-- <ul v-bind:key="index" v-for="(technology, index) in backend_technologies"> -->
        {{ technology }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para front-end:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
    </ul>
  <!-- <ul v-bind:key="index" v-for="(technology, index) in frontend_technologies">
    <li>{{ technology }}</li>
    </ul>   -->
    <button @click="showEmail">{{ textoBotao }}</button>
  <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
  <p class="teste">Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
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
        textoBotao: 'Mostrar e-mail',
        backend_technologies: ["JavaScript", "PHP", "Python"],
        // frontend_technologies: ["HTML", "CSS", "Vue"]
        frontend_technologies: [
          {id: 1, language: 'HTML'},
          {id: 2, language: 'CSS'},
          {id: 3, language: 'Vue'}
        ]
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

<style>
  .paragrafo-pai {
    color: red;
  }
</style>