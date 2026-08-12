<template>
  <div>
    <Header />    
    <PrimeiroComponente />
    <p class="paragrafo-pai">O dado de app é: {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
  import Header from './components/Header'
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue';

  export default {
    name: 'App',
    components: {
      Header,
      PrimeiroComponente,
      LifeCycle,
      Pessoa
    },
    data() {
      return {
        testando: "Teste"
      }
    }
  }
</script>

<style>
  body {
    background-color: #333;
    color: #FFF;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000 
  }
</style>