<script setup>
const mensagem = 'Kauã'

function inverter(texto) {
  return texto.split('').reverse().join('')
}

</script>

<template>
  <p> {{ inverter(mensagem) }}</p>
</template>