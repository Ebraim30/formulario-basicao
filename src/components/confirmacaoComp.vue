<script setup>
import { ref } from 'vue';
const confirmacao = ref('')

</script>


<template>
  
  <p>Confirme sua Senha</p>
    <input type="password" v-model="confirmacao" size="20" maxlength="20" placeholder="Confirme sua senha" />   
  
    <div>Confirma sua senha: {{ confirmacao }}</div>
          <hr /> 
</template>

