<script setup>
import { ref } from 'vue';

const registrar = ref(false)


 
const nome = ref ('')
const email = ref ('')
const senha = ref ('')
const confirmacao = ref ('')
const profissao = ref ('')
const salario = ref ('')
const cpf = ref  ('')
const linguagens = ref ('')
const idade = ref ('') 
const Endereco = ref ('')
const cidade = ref ('')
const data = ref ('')
const biografia = ref ('')

function deletar (apagado) {
  nome.value = ('')
  email.value = ('')
  senha.value = ('')
  confirmacao.value = ('')
  profissao.value = ('')
  salario.value = ('')
  cpf.value = ('')
  linguagens.value = ('')
  idade.value = ('')
  Endereco.value = ('')
  cidade.value = ('')
  data.value = ('')
  biografia.value = ('')
  registrar.value = (false)
}

function edit (editar) {
  nome.value = nome.value
  email.value = email.value
  senha.value = senha.value
  confirmacao.value = confirmacao.value
  profissao.value = profissao.value
  salario.value = salario.value
  cpf.value = cpf.value
  linguagens.value = linguagens.value
  idade.value = idade.value
  Endereco.value = Endereco.value
  cidade.value = cidade.value
  data.value = data.value  
  biografia.value = biografia.value
  registrar.value = (false)
}

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
    <input type="password" v-model="confirmacao" size="20" maxlength="20" placeholder="Confirme sua senha">
    <p>Informe sua profissao</p>
    <input type="text" v-model="profissao" size="20" maxlength="30" placeholder="Digite sua Profissão">
    <p>Informe seu salario</p>
    <input type="password" v-model="salario" size="20" maxlength="30" placeholder="Digite seu salario">
    <p>Informe seu cpf: </p>
    <input type="password" v-model="cpf" size="20" maxlength="11" placeholder="Digite seu CPF">
    <p>Informe sua idade: </p>
    <input type="number" v-model="idade" size="20" placeholder="Digite sua idade">
    <p>Informe a Data</p>
    <input type="date" v-model="data" placeholder="Digite a Data">
    <p>Informe seu Endereco</p>
    <input type="string" v-model="Endereco" size="20" maxlength="55" placeholder="Digite sua Rua e Nº">
    <p>Informe seu Estado</p>
    <select v-model="cidade">
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


  <div class="user-cards">
    <button  @click="$event => registrar = !registrar">Registrar</button> 
    <div class="card">Dados Salvos
    <div v-if="registrar" class="card-content">
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
      Senha: {{ confirmacao }}
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
      Endereco: {{ Endereco }}
    </div>
    <hr>
    <div>
      Estado: {{ cidade }}
    </div>
    <hr>
    <div>
      Biografia: {{ biografia }}
    </div>
    <hr>
    <div>
      Linguagem: {{ linguagens }}
    </div>
    <button @click="deletar(apagado)">Deletar</button>
    <button @click="edit(editar)">Editar</button>
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

.user-cards {
    display: flow-root;
    flex-wrap: wrap;
    justify-content: flex-end;
    margin-top: 20px;
  }

  .card {
    flex: 0 0 300px;
    background-color: #8900fa;
    border-radius: 15px;
    box-shadow: 0 2px 4px rgb(255, 0, 0);
    margin-right: 20px;
    margin-bottom: 20px;
  }

  .card-content {
    padding: 30px;
  }

  .card button {
    padding: 5px 10px;
    margin-top: 10px;
    border-radius: 3px;
    border: none;
    color: #4b398b;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  .card button.edit {
    background-color: #ffeb3b; 
  }

  .card button.edit:hover {
    background-color: #fdd835; 
  }

  .card button.delete {
    background-color: #f44336; 
  }

  .card button.delete:hover {
    background-color: #e53935; 
  }
</style>
