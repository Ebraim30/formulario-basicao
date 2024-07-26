<script setup>
import { ref } from 'vue';
const nome = ref('')

  

</script>
<template>
<p>Informe seu nome:</p>
    <input type="text" v-model="nome" size="20" maxlength="20" placeholder="Digite seu nome" />
    <div>Nome: {{ nome }}</div>
          <hr />    
</template>

<style setup>
    
</style>

