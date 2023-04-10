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
const lingProg = ref('')
const bio = ref('')
const enviar = ref(false)

</script>

<template>
  <h1 class="titulo">FORMS</h1>
  <form @submit.prevent="enviar">
    <div class="informacao">
      <p>Digite seu nome: </p>
      <input type="text" v-model="nome" />
      <p>Digite seu email: </p>
      <input type="email" v-model="email" />
      <p>Digite sua senha: </p>
      <input type="password" v-model="senha" maxlength="8" />
      <p>Confirme sua senha: </p>
      <input type="password" v-model="confirmacao" maxlength="8"/>
      <p>Informe sua data de nascimento: </p>
      <input type="data" v-model="nascimento" />
      <p>Informe seu endereço:</p>
      <input type="text" v-model="endereco" />
      <p>Informe a cidade que você mora:</p>
      <input type="string" v-model="cidade" />
      <p>Informe o estado que você mora:</p>
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
      <p>hobbies:</p>
      <input type="text" v-model="hobbies" />
      <p>Linguagens De Programação:</p>
      <input type="text" v-model="lingProg" />
      <p>Biografia:</p>
      <input type="text" v-model="bio" />
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
    <p>Nome: {{ nome }}</p>
    <input type="text" v-model="nome" readonly />
    <p>E-mail: {{ email }}</p>
    <input type="text" v-model="email" readonly />
    <p>Senha: {{ senha }}</p>
    <input type="text" v-model="senha" readonly />
    <p>Senha Confirmada: {{ confirmacao }}</p>
    <input type="text" v-model="confirmacao" readonly />
    <p>Data de Nascimento: {{ nascimento }}</p>
    <input type="text" v-model="nascimento" readonly />
    <p>Endereço: {{ endereco }}</p>
    <input type="text" v-model="endereco" readonly />
    <p>Cidade: {{ cidade }}</p>
    <input type="text" v-model="cidade" readonly />
    <p>Estado: {{ estado }}</p>
    <input type="text" v-model="estado" readonly />
    <p>Biografia: {{ bio }}</p>
    <input type="text" v-model="bio" readonly />

  </div>

</template>






