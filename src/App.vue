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
</script>

<template>
      <div>
      <p>Digite seu nome: </p>
        <input type="text" v-model="nome" />
    </div>
        <div> 
        <p>Digite seu email: </p>
        <input type="email" v-model="email" />
        </div>
        <div>
          <p>Digite sua senha: </p>
        <input type="password" v-model="senha" />
        <div>
          <p>Confirme sua senha: </p>
          <input type="password" v-model="confirmacao" />
        </div>
        </div>
        <div>
          <p>Data de nascimento: </p>
          <input type="number" v-model="nascimento" />
        </div>
        <div>
          <p>Endereço:</p>
          <input type="text" v-model="endereco" />
        </div>
        <div>
          <p>cidade:</p>
          <input type="string" v-model="cidade" />
        </div>
        <p>Estado:</p>
          <input type="select" v-model="estado" />
        </div>
</template>


