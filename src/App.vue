<script setup>
const rawHtml = '<span style="color: red">Este é um texto em vermelho</span>'
</script>

<template>
  <p>Usando a interpolação de texto: {{ rawHtml }}</p>
  <p>Usando a diretiva v-html: <span v-html="rawHtml"></span></p>
</template>