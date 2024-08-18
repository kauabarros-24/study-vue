<script setup>
import { ref } from 'vue';

const contador = ref(0)
const nome = "Kauã"
const idade = 16

function inverter(texto){
   return nome.split('').reverse().join('').toUpperCase()
}

function saudacao() {
  return `Olá ${nome}`
}

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  contador.value--
}
function zerar() {
  contador.value = 0
}

</script>

<template>
  <div class="info">
        <h1>Exemplo 1 - Mostrando informações na tela</h1>
        <p>Nome: {{ nome }} </p>
        <p>Idade: {{ idade }}  anos</p>
        <hr />
        <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
        <p>O nome tem {{ nome.length }}  caracteres</p>
        <p>O nome invertido é: {{ inverter(nome) }} </p>
        <hr />
        <p> Exemplo de saudação usando função</p>
        <p> {{ saudacao() }}  </p>
    </div>

  <div class="contador">
    <h1>Exemplo 2: Contador</h1>
    <button @click="incrementarContador">Incrementar</button>
    <button @click="decrementarContador">Decrementar</button>
    <button @click="zerar">Zerar</button>
    <hr>
    <p> Contador: {{ contador }} </p>
    <hr>
    <div class="maior" v-if="contador >= 10"><p>O valor do contador é maior que 10</p></div>
    <div class="menor" v-else><p>O valor do contador é menor que 10</p></div>
    
  </div>
</template>

<style scoped>
.info, .contador {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  margin-left: 10px;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
button {
  margin-top: 10px;
  margin-bottom: 10px;
  margin-right: 10px;
}
.maior {
  color: green
}
.menor {
  color: red;
}
p {
  margin-top: 5px;
  margin-bottom: 5px;
}
</style>