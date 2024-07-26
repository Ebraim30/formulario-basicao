<script setup>
import { normalizeStyle, ref } from 'vue'
import { reactive } from 'vue'
import Swal from 'sweetalert2'
import NomeComp from './components/NomeComp.vue'
import senhaComp from './components/senhaComp.vue'
import confirmacaoComp from './components/confirmacaoComp.vue'
import emailComp from './components/emailComp.vue'
import profissaoComp from './components/profissaoComp.vue'
import salarioComp from './components/salarioComp.vue'
import cpfComp from './components/cpfComp.vue'
const registrar = ref(false)

const user = reactive({
  avatar: null
})






const linguagens = ref('')
const idade = ref('')
const Endereco = ref('')
const cidade = ref('')
const data = ref('')
const biografia = ref('')

function deletar(apagado) {
  nome.value = ''
  email.value = ''
  senha.value = ''
  confirmacao.value = ''
  profissao.value = ''
  salario.value = ''
  cpf.value = ''
  linguagens.value = ''
  idade.value = ''
  Endereco.value = ''
  cidade.value = ''
  data.value = ''
  biografia.value = ''
  registrar.value = false
}

function edit(editar) {
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
  registrar.value = false
}

function save() {
  let error = false
  const campos = []

  if (email.value == '' || email.value == null) {
    campos.push('email ')
    error = true
  }

  if (senha.value == '' || senha.value == null) {
    campos.push('senha ')
    error = true


  }
  if (confirmacao.value == '' || confirmacao.value == null) {
    campos.push('confirmação ')
    error = true

  }
  if (profissao.value == '' || profissao.value == null) {
    campos.push('profissâo ')
    error = true

  }
  if (salario.value == '' || salario.value == null) {
    campos.push('salario ')
    error = true
  }
  if (cpf.value == '' || cpf.value == null) {
    campos.push('CPF ')
    error = true
  }
  if (linguagens.value == '' || linguagens.value == null) {
    campos.push ('Linguagens ')
 error = true

   }
   if (idade.value == '' || idade.value == null) {
    campos.push ('Idade ')
 error = true 
  }
  if (Endereco.value == '' || Endereco.value == null) {
campos.push ('Endereço ')
error = true
  }
   if (cidade.value == '' || cidade.value == null) {
campos.push ('Cidade ')
error = true
   }
   if (data.value == '' || data.value == null) {
  campos.push ('Data ')
error = true
}

   if (biografia.value == '' || biografia.value == null) {
  campos.push ('biografia ')
  error = true
  }


  if (!error) {
    registrar.value = true
  } else {
    Swal.fire({
      title: "Atenção",
      text: `Você esqueceu dos campos: ${campos}!`,
      icon: "error"
    });
  }

}


function handleFileUpload(e) {
  const target = e.target
  if (target && target.files) {
    const file = target.files[0]
    user.avatar = URL.createObjectURL(file)
  }
}

</script>

<template>
  <div class="formulario">
    <h1>Informe seus dados</h1>

    <input type="file" id="avatarField" @change="handleFileUpload($event)" />
    <img v-if="user.avatar" :src="user.avatar" />

    <NomeComp />
    <senhaComp />
    <confirmacaoComp />
    <emailComp />
    <profissaoComp />
    <salarioComp />
<cpfComp />

    <p>Informe sua idade:</p>
    <input type="number" v-model="idade" size="20" placeholder="Digite sua idade" />
    <p>Informe a Data</p>
    <input type="date" v-model="data" placeholder="Digite a Data" />
    <p>Informe seu Endereco</p>
    <input type="string" v-model="Endereco" size="20" maxlength="55" placeholder="Digite sua Rua e Nº" />
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
    <hr />
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
    <hr />
    <p>Biografia</p>
    <textarea v-model="biografia" cols="30" rows="10"></textarea>

    <div class="user-cards">

      <button @click="save()">Registrar</button>
      <div class="card">
        Dados Salvos
        <div v-if="registrar" class="card-content">
          <div>Foto: <img :src="user.avatar" /></div>
        
         
          <div>Idade: {{ idade }}</div>
          <hr />
          <div>Data: {{ data }}</div>
          <hr />
          <div>Endereco: {{ Endereco }}</div>
          <hr />
          <div>Estado: {{ cidade }}</div>
          <hr />
          <div>Biografia: {{ biografia }}</div>
          <hr />
          <div>Linguagem: {{ linguagens }}</div>
          <button @click="deletar(apagado)">Deletar</button>
          <button @click="edit(editar)">Editar</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.formulario {
  box-shadow: 2px 6px 6px rgb(255, 0, 0);
  border-radius: 50px;
  text-align: center;
  padding: 100px;
  background-color: rgba(100, 88, 146, 0.514);
  margin: 0px auto;

}

.salvas {
  border-radius: 40px;
  text-align: center;
  padding: 30px;
  color: rgb(0, 0, 0);
  position: fixed;
}

h1 {
  color: rgb(231, 16, 16);
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
  background-color: rgba(100, 88, 146, 0.514) ;
  border-radius: 15px;
  box-shadow: 0 2px 4px rgb(255, 0, 0);
  margin-right: 0px;
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
  color: #bd1313;
  cursor: pointer;
  transition: background-color 0.3s ease;
}
</style>
