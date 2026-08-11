<template>
  <div>
    <h1>Meu nome é: {{ nome }}</h1>
    <Info />
  </div>
</template>

<script>
import Info from './Info.vue'

export default {
  name: 'LifeCycle',
  components: {
    Info
  },
  data() {
    return { 
      nome: "Ainda não sei"
    }
  },
  created() {
    setTimeout(() => {
      this.nome = "Matheus"
    }, 1000);
  },
  mounted() {
      setTimeout(() => {
        this.nome = "Pedro"
      }, 2000);
  }
}

</script>