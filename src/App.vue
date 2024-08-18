<script setup>
import { c } from 'vite/dist/node/types.d-aGj9QkWt';
import { ref } from 'vue';

const contador = ref(0)

function incrementarContador(){
  contador.value++
}

function decrementarContador() {
  if (contador.value > 0) {
    contador.value--
  }
}

</script>

<template>
  <button @click="incrementarContador">Incrementar</button> 
  <button @click="decrementarContador">Decrementar</button>
  <p>Valor do contador: {{ contador }}</p>
</template>

<style>
button {
  font-weight: bold;
}</style>