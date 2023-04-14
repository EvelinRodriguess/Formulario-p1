<script setup>
import { ref } from 'vue'
const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmacao = ref('')
const nascimento = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const lingProg = []
const bio = ref('')
const enviar = ref(false)
const erro = ref('')

function validacao() {
  erro.value = ''

  if (!nome.value) {
    erro.value = 'Por favor, digite seu nome.'
    return
  }

  if (!email.value) {
    erro.value = 'Por favor, digite seu e-mail.'
    return
  }

  if (!senha.value) {
    erro.value = 'Por favor, digite sua senha.'
    return
  }

  if (senha.value !== confirmacao.value) {
    erro.value = 'A senha e a confirmação de senha não são iguais.'
    return
  }

  enviar.value = true
}
</script>

<template>
  <h1 class="titulo">FORMS</h1>
  <form @submit.prevent="validacao">

    <div class="informacao">

      <label for="nome">Nome</label>
      <input type="text" v-model="nome" placeholder="Digite seu nome" />

      <label for="email">E-mail</label>
      <input type="email" v-model="email" placeholder="Digite seu e-mail" />

      <label for="senha">Senha</label>
      <input type="password" v-model="senha" maxlength="8" placeholder="Crie sua senha" />

      <label for="confirmacao">Confirmação de senha</label>
      <input type="password" v-model="confirmacao" maxlength="8" placeholder="Confirme a senha" />

      <label for="nascimento">Data de nascimento</label>
      <input type="date" v-model="nascimento" placeholder="Digite sua data de nascimento" />

      <label for="endereco">Endereço</label>
      <input type="text" v-model="endereco" placeholder="Digite seu endereço" />

      <label for="cidade">Cidade</label>
      <input type="string" v-model="cidade" placeholder="Digite o nome de sua cidade"  />

      <label for="estado">Estado</label>
      <select v-model="estado">
        <option value="ac">ACRE</option>
        <option value="al">ALAGOAS</option>
        <option value="ap">AMAPA</option>
        <option value="am">AMAZONAS</option>
        <option value="ba">BAHIA</option>
        <option value="ce">CEARA</option>
        <option value="df">DISTRITO FEDERAL</option>
        <option value="es">ESPIRITO SANTO</option>
        <option value="go">GOIAS</option>
        <option value="ma">MARANHÃO</option>
        <option value="mt">MATO GROSSO</option>
        <option value="ms">MATO GROSSO DO SUL</option>
        <option value="mg">MINAS GERAIS</option>
        <option value="pa">PARÁ</option>
        <option value="pb">PARAIBA</option>
        <option value="pr">PARANÀ</option>
        <option value="pe">PERNAMBUCO</option>
        <option value="pi">PIAUÍ</option>
        <option value="rj">RIO DE JANEIRO</option>
        <option value="rn">RIO GRANDE DO NORTE</option>
        <option value="rs">RIO GRANDE DO SUL</option>
        <option value="ro">RONDONIA</option>
        <option value="rr">RORAIMA</option>
        <option value="sc">SANTA CATARINA</option>
        <option value="sp">SÃO PAULO</option>
        <option value="se">SERGIPE</option>
        <option value="to">TOCANTINS</option>
      </select>
      
      <label for="hobbies"> Hobbies </label>
      <input type="checkbox" v-model="hobbies" value="volei"/> VOLEI
      <input type="checkbox" v-model="hobbies" value="fut" /> FUTEBOL
      <input type="checkbox" v-model="hobbies" value="ler" /> LER
      <input type="checkbox" v-model="hobbies" value="out" /> OUTROS

      <label for="lingProg">Linguagens de programação </label>
      <input type="checkbox" v-model="lingProg" value="php" /> PHP
      <input type="checkbox" v-model="lingProg" value="ja" /> JAVA
      <input type="checkbox" v-model="lingProg" value="js" /> JAVASCRIPT
      <input type="checkbox" v-model="lingProg" value="py" /> PYTHON
      <input type="checkbox" v-model="lingProg" value="C" /> C++
      <input type="checkbox" v-model="lingProg" value="ts" /> TYPESCRIPT
      <input type="checkbox" v-model="lingProg" value="out" /> OUTRA

      <label for="bio">Biografia</label>
      <input type="text" v-model="bio" placeholder="Conte um pouco sobre você" />

    </div>
    <br>
    
    <button @click="enviar">enviar</button>

    <br>
  </form>

  <hr>

  <div class="dados">
   <br>

    <p class="titulo">Dados Preenchidos:</p>
    <br>
    
    <label for="nome">Nome informado</label>
    <input type="text" v-model="nome" readonly />

    <label for="email">E-mail informado</label>
    <input type="text" v-model="email" readonly />

    <label for="senha">Senha informada</label>
    <input type="text" v-model="senha" readonly />

    <label for="confirmacao">Senha confirmada</label>
    <input type="text" v-model="confirmacao" readonly />

    <label for="nascimento">Data de nascimento informada</label>
    <input type="text" v-model="nascimento" readonly />

    <label for="endereco">Endereço inforamado</label>
    <input type="text" v-model="endereco" readonly />

    <label for="cidade">Cidade informada</label>
    <input type="text" v-model="cidade" readonly />

    <label for="estado">Estado informado</label>
    <input type="text" v-model="estado" readonly />


    <label for="hobbies">Hobbie informado</label>
    <input type="text" v-model="hobbies" readonly />

    <label for="bio">Liguagens de programação informada</label>
    <input type="text" v-model="lingProg" readonly />

    <label for="bio">Biografia</label>
    <input type="text" v-model="bio" readonly />
  </div>

</template>

<style>

  .titulo {
    text-align: center;
    font-size: 2rem;
  }

  form {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .informacao {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 1rem;
  }

  select {
    width: 100%;
    padding: 0.5rem;
    margin-top: 0.5rem;
    margin-bottom: 1rem;
    font-size: 1rem;
    border-radius: 5px;
    border: 1px solid #ccc;
  }

  input[type="text"],
  input[type="email"],
  input[type="password"],
  input[type="data"] {
    width: 100%;
    padding: 0.5rem;
    margin-top: 0.5rem;
    margin-bottom: 1rem;
    font-size: 1rem;
    border-radius: 5px;
    border: 1px solid #ccc;
  }

  button {
    padding: 0.5rem 1rem;
    font-size: 1rem;
    border-radius: 5px;
    border: none;
    background-color: #0077cc;
    color: white;
    cursor: pointer;
  }

  .dados {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 2rem;
  }

  .dados p {
    margin-top: 0.5rem;
    margin-bottom: 1rem;
    font-size: 1rem;
    font-weight: bold;
  }

  .dados input[type="text"] {
    width: 100%;
    padding: 0.5rem;
    margin-top: 0.5rem;
    margin-bottom: 1rem;
    font-size: 1rem;
    border-radius: 5px;
    border: 1px solid #ccc;
    background-color: #f0f0f0;
  }
</style>






