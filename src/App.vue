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
    <label for="nome" style="margin-left: 20px;">Nome: </label>
    <input type="text" placeholder="informe a Nome" size="20" v-model.lazy="nome" />
    <label for="senha" style="margin-left: 20px;">Senha</label>
    <input type="password" placeholder="informe a senha" size="20" minlength="3" v-model="senha" />
    <!--minlength é minimo de letra -->
    <label for="idade" style="margin-left: 20px;">Idade</label>
    <input type="number" v-model="idade" />
    <!-- :value="texto" @input="(e) => (texto=e.target.value)" -->
  </div>
  <div>
  <br>
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
  <select v-model="tamanho">
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
