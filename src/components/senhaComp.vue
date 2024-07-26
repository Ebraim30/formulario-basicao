<script setup>
import { ref } from 'vue';
const senha = ref('')

</script>

 <template>
<p>Informe sua senha:</p>
    <input type="password" v-model="senha" size="20" maxlength="20" placeholder="Digite sua senha:" />
    <div>Senha: {{ senha }}</div>
 </template>

