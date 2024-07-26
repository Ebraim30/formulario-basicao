<script setup>

import { ref } from 'vue';
const email = ref('')

</script>


<template>
<p>Informe seu email:</p>
    <input type="email" v-model="email" size="20" maxlength="30" placeholder="Digite seu email" />

    <div>Nome: {{ email }}</div>
          <hr />   
          
</template>


<style scoped>

</style>