<script setup>
import { ref } from 'vue';
const profissao = ref('')

  

</script>
<template>
<p>Informe sua Profissão:</p>
    <input type="text" v-model="profissao" size="20" maxlength="20" placeholder="Digite sua profissao   " />
    <div>Profissão: {{ profissao }}</div>
          <hr />    
</template>