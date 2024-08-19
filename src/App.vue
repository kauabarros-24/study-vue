<script>
import { reactive, computed } from 'vue';

const professor = reactive({
  nome: 'Eduardo da Silva',
  disciplinas: [
    'Desenvolvimento web',
    'Desenvolimento de aplicações móveis',
  ],
})

const possuiDisciplinas = computed(() => {
  return professor.disciplinas.lenght > 0
})
</script>

<template>
  <div>
    <h1>Professor</h1>
    <p>Nome: {{ professor.nome }}</p>
  </div>
</template>