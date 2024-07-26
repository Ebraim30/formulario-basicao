<script setup>
import { ref } from 'vue';
const cpf = ref('')

</script>

 <template>
<p>Informe seu cpf:</p>
    <input type="password" v-model="cpf" size="20" maxlength="20" placeholder="Digite seu CPF:" />
    <div>Senha: {{ cpf }}</div>
 </template>

 