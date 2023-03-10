<script setup>
  import { ref } from 'vue'
    const nome = 'Rafaella'
    const idade = 16

    function inverter(texto) {
        return texto.split('').reverse().join('')
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }

    let valor1 = ref("");
    function mostrarDobro() {
      return `O dobro do ${valor1.value} é ${valor1.value * 2}`
    }
    
    let valor2 = ref('');
    let valor3 = ref("");
    function soma() {
      return `A soma dos números resulta em ${(valor2.value * 1) + (valor3.value * 1)}`;
    } 
    function somaPar() {
      if (soma.value % 2 === 0) {
      return `A soma é par`
    }}
    
</script>

<template>
  <div class="info">
    <h1>Exemplo 1 - Mostrando informações na tela</h1>
    <p>Nome: {{ nome }} </p>
    <p>Idade: {{ idade }}  anos</p>
    <hr />
    <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
    <p>O nome tem {{ nome.length }}  caracteres</p>
    <p>O nome invertido é: {{ (inverter(nome)).toUpperCase() }} </p>
    <hr />
    <p> Exemplo de saudação usando função</p>
    <p> {{ saudacao() }}  </p>
    <hr />
    <input v-model="valor1">
    <p> {{ mostrarDobro() }} </p>
    <hr />
    <input v-model="valor2">
    <input v-model="valor3">
    <p> {{ soma() }} </p>
    <hr />
    <p>{{ somaPar }}</p>
  </div>
</template>

<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
</style>
