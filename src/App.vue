<script setup>
import { ref } from 'vue'

const nome = ref('')
const senha = ref('')
const idade = ref('')
const bio = ref('')
const aceitaTermos = ref(false)
const cores = ref([])
const sexo = ref('')
const tamanho = ref('')
</script>

<template>
  <div>
    <label for="nome">Nome: </label>
    <input type="text" size="20" v-model="nome" />
    <label for="senha">Senha</label>
    <input type="password" size="20" minlength="3" v-model="senha" />
    <!--minlength é minimo de letra -->
    <label for="idade">Idade</label>
    <input type="number" v-model="idade" />
    <!-- :value="texto" @input="(e) => (texto=e.target.value)" -->
  </div>
  <div>
    <textarea v-model="bio" cols="100" rows="3" />
  </div>
  <label for="aceitaTermos">possui carro(s)?</label>
  <input type="checkbox" v-model="aceitaTermos" />
  <hr />

  <label for="cores">Cores favoritas</label>
  <input type="checkbox" v-model="cores" value="vermelho" /> Vermelho
  <input type="checkbox" v-model="cores" value="verde" /> Verde
  <input type="checkbox" v-model="cores" value="azul" /> Azul

  <hr />

  <label for="sexo">Sexo</label>
  <input type="radio" v-model="sexo" value="masculino" /> Masculino
  <input type="radio" v-model="sexo" value="feminino" /> Feminino

<hr>

<label for="tamanho">tamanho</label>
  <select v-model="sexo">
    <option value="p">p</option>
    <option value="m">m</option>
    <option value="gg">gg</option>
  </select>

  <div>
    <p>nome: {{ nome }}</p>
    <hr />
    <p>senha: {{ senha }}</p>
    <hr />
    <p>idade: {{ idade }}</p>
    <hr />
    <p>bio: {{ bio }}</p>
    <hr />
    <p>possui carro(s): {{ aceitaTermos }}</p>
    <hr />
    <p>Cores favoritas:{{ cores }}</p>
    <hr>
    <p>Sexo: {{ sexo }} </p>
    <hr>
    <p>tamanho: {{ tamanho }}</p>
  </div>
</template>

<style scoped></style>
