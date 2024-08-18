<script>
  export default {
    data() {
      return {
        contador: 0
      }
    },
    methods: {
      incrementarContador() {
        this.contador++
      },
      decrementarContador() {
        if (this.contador > 0) {
          this.contador--
        }
      },
      mounted() {
        console.log(`O valor do contador é ${this.contador}`)
      }
    }
  }

</script>

  <template>
    <button @click="incrementarContador">Incrementar</button> 
    <button @click="decrementarContador">Decrementar</button>
    <p>Valor do contador: {{ contador }}</p>
  </template>

  <style scoped>
  button {
    font-weight: bold;
  }

  </style>