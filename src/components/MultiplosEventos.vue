<template>
  <div>
    <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro()">
      Ativar múltiplos eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>
<script>
export default {
  name: 'MultiplosEventos',
  // components: {
    data() {
      return {
        multiplos_eventos: "",
        txt1: "Primeiro evento",
        txt2: "Segundo evento"
      }
    },
  methods: {
    // primeiro() {
    //   this.multiplos_eventos = "Primeiro evento"
    primeiro(txt, e) {
      this.multiplos_eventos = txt;
    },
    segundo(txt, e) {
      setTimeout(() => this.multiplos_eventos = txt, 1500)
    },
    terceiro() {
      setTimeout(() => this.multiplos_eventos = "", 3000)
    }
  }
}
</script>
<style scoped>
  div {
    margin: 100px;
  }
</style>