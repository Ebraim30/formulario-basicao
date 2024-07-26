<script setup>
import { ref } from 'vue';
const salario = ref('')

</script>

 <template>
<p>Informe seu salario:</p>
    <input type="password" v-model="salario" size="20" maxlength="20" placeholder="Digite seu salario:" />
    <div>Senha: {{ salario }}</div>
 </template>

 