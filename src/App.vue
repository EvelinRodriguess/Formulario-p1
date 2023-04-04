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
</script>

<template>
  <form @submit.prevent="enviar">
    <div>
      <p>Digite seu nome: </p>
      <input type="text" v-model="nome" />
      <p>Digite seu email: </p>
      <input type="email" v-model="email" />
      <p>Digite sua senha: </p>
      <input type="password" v-model="senha" />
      <p>Confirme sua senha: </p>
      <input type="password" v-model="confirmacao" />
      <p>Data de nascimento: </p>
      <input type="data" v-model="nascimento" />
      <p>Endereço:</p>
      <input type="text" v-model="endereco" />
      <p>cidade:</p>
      <input type="string" v-model="cidade" />
      <p>Estado:</p>
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
    <button type='submit'> enviar</button>
  </form>

  <div>
    <p>Dados Preenchidos</p>

      <p>Nome: {{ nome }}</p>
      <p>E-mail: {{ email }}</p>
      <p>Senha: {{ senha }}</p>
      <p>Senha Confirmada: {{ confirmacao }}</p>
      <p>Data de Nascimento: {{ nascimento }}</p>
      <p>Endereço: {{ endereco }}</p>
      <p>Cidade: {{ cidade }}</p>
      <p>Estado: {{ estado }}</p>
      <p>Biografia: {{ bio }}</p>

  </div>
</template>


