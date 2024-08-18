<script setup>
import { ref, onMounted } from 'vue';

const contador = ref(0);

const incrementarContador = () => contador.value++
const decrementarContador = () => contador.value > 0 ? contador.value-- : contador.value



</script>

<template>
  <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <p> {{ contador }}</p>

</template>

<style scoped>
button {
  font-weight: bold;
}
</style>