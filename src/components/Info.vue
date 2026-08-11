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
  <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
   <p v-if="4 > 2">Testando</p>
</div>  
</template>
<script>

export default {
  name: 'Info',
  // components: {
    //   Picture
    data() {
      return { 
        esta_trabalhando: false,
        mostrar_email: true,
        email: 'matheus@email.com'
        // url_portfolio: "https://www.google.com"
      }
    }
  }
// }
</script>