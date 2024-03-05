<script setup>
import { ref } from 'vue';


const Registro = ref(false)

const nome = ref ('')
const cpf = ref  ('')
const idade = ref ('') 



</script>

<template>
  <div class="formulario">
    <h1> Informe essas informacoes </h1>
    <p>Informe seu nome: {{ nome }} <input type="string" v-model="nome" size="20" maxlength="20"></p>
    <p>Informe seu cpf: {{ cpf }} <input type="password" :type="Number" v-model="cpf" size="20" maxlength="11"></p>
    <p>Informe sua idade: {{ idade }} <input type="number" v-model="idade" size="20"></p>
    <p>concorde com os termos para prosseguir <input type="checkbox" v-model="aceitaTermos" /></p>
    
    <hr>

  <div class="salvas">
    <button @click="$event => !Registro"></button>
    <div>
      Nome: {{ nome }}
      <hr>
      CPF: {{ cpf }}
      <hr>
      Idade: {{ idade }}
    </div>
    </div>
  </div>

</template>

<style scoped>
.formulario {
  background-color: rgb(162, 0, 255);
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
