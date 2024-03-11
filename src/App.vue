<script setup>
import { ref } from 'vue';

const registrar = ref(false)



const nome = ref ('')
const email = ref ('')
const senha = ref ('')
const confirma = ref ('')
const profissao = ref ('')
const salario = ref ('')
const cpf = ref  ('')
const linguagens = ref ('')
const idade = ref ('') 
const morador = ref ('')
const data = ref ('')
const biografia = ref ('')


</script>

<template>
  <div class="formulario">
    <h1> Informe essas informacoes </h1>
    <p>Informe seu nome: </p>
    <input type="text" v-model="nome" size="20" maxlength="20" placeholder="Digite seu nome">
    <p>Informe seu email:</p>
    <input type="email" v-model="email" size="20" maxlength="30" placeholder="Digite seu email">
    <p>Informe sua senha:</p>
    <input type="password" v-model="senha" size="20" maxlength="20" placeholder="Digite sua senha:">
    <p>Confirme sua Senha</p>
    <input type="password" v-model="confirma" size="20" maxlength="20" placeholder="Confirme sua senha">
    <p>Informe sua profissao</p>
    <input type="text" v-model="profissao" size="20" maxlength="30" placeholder="Digite sua Profissão">
    <p>Informe seu salario</p>
    <input type="password" :type="Number" v-model="salario" size="20" maxlength="30" placeholder="Digite seu salario">
    <p>Informe seu cpf: </p>
    <input type="password" :type="Number" v-model="cpf" size="20" maxlength="11" placeholder="Digite seu CPF">
    <p>Informe sua idade: </p>
    <input type="number" v-model="idade" size="20" placeholder="Digite sua idade">
    <p>Informe a Data</p>
    <input type="date" v-model="data" placeholder="Digite a Data">
    <p>Informe seu Estado</p>
    <select v-model="morador">
      <option value="AC">Acre</option>
      <option value="AL">Alagoas</option>
      <option value="AP">Amapa</option>
      <option value="AM">Amazonas</option>
      <option value="BA">Bahia</option>
      <option value="CE">Ceara</option>
      <option value="ES">Espirito Santo</option>
      <option value="GO">Goias</option>
      <option value="MA">Maranhao</option>
      <option value="MT">Mato Grosso</option>
      <option value="MS">Mato Grosso do Sul</option>
      <option value="MG">Minas Gerais</option>
      <option value="PA">Para</option>
      <option value="PB">Paraiba</option>
      <option value="PR">Parana</option>
      <option value="PE">Pernambuco</option>
      <option value="PI">Piaui</option>
      <option value="RJ">Rio de Janeiro</option>
      <option value="RN">Rio Grande do Norte</option>
      <option value="RS">Rio Grande do Sul</option>
      <option value="RO">Rondonia</option>
      <option value="RR">Roraima</option>
      <option value="SC">Santa Catarina</option>
      <option value="SP">Sao Paulo</option>
      <option value="SE">Sergipe</option>
      <option value="TO">Tocantins</option>
      <option value="DF">Distrito Federal</option>
    </select>
    <hr>
    <p>Escolha uma Linguagem</p>
    <select v-model="linguagens">
    <option value="JS">Javascript</option>
    <option value="VUE">VUEJS</option>
    <option value="HTML">HTML4</option>
    <option value="C++">C++</option>
    <option value="C#">C#</option>
    <option value="CSS">CSS</option>
    <option value="PHP">PHP</option>
    <option value="Python">Python</option>
    <option value="Django">Django</option>
    </select>
    <hr>
    <p>Fale um pouco sobre voce</p>
    <textarea v-model="biografia" cols="30" rows="10"></textarea>


  <div class="salvas">
    <button  @click="$event => registrar = !registrar">Registrar</button>
    <div v-if="registrar">
      <div>
      Nome: {{ nome }}
    </div>
      <hr>
    <div>
      Email: {{ email }}
    </div>
    <hr>
    <div>
      Senha: {{ senha }}
    </div>
    <hr>
    <div>
      Senha: {{ confirma }}
    </div>
    <hr>
    <div>
      Profissao: {{ profissao }}
    </div>
    <hr>
    <div>
      Salario: {{ salario }}
    </div>
    <hr>
      <div>
      CPF: {{ cpf }}
    </div>
      <hr>
      <div>
      Idade: {{ idade }}
    </div>
    <hr>
    <div>
      Data: {{ data }}
    </div>
    <hr>
    <div>
      Estado: {{ morador }}
    </div>
    <hr>
    <div>
      Biografia: {{ biografia }}
    </div>
    <hr>
    <div>
      Linguagem: {{ linguagens }}
    </div>
    </div>
    </div>
  </div>

</template>

<style scoped>
.formulario {
  border: 5px solid;
  border-radius: 50px;
  text-align: center;
  padding: 25px;
  background-color: blue;
  margin: 0px auto;
  border-color: blueviolet;
}
.salvas {
  border-radius: 40px;
  text-align: center;
  padding: 30px;
  color: rgb(255, 255, 255);
}


h1 {
  color: white;
  font-weight: bold 10px;
  font-size: 30px;
}
</style>
