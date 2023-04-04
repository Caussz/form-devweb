<script setup>
import { ref, computed } from 'vue'

const usuario = ref({
  nome: String,
  idade: Number,
  dm: Date,
  estado: String,
  cidade: String,
  endereco: String,
  hobbies: String,
  lingProg: String,
  bio: String
})

const name = ref(' ')
const age = ref(0)
const date = ref(' ')
const state = ref(' ')
const adress = ref(' ')
const hobbi = ref(' ')
const langP = ref(' ')
const biografia = ref(' ')

const confirma = computed((nome, idade, dm, estado, cidade, endereco, hobbies, lingProg, bio) => {
  usuario.value.nome = nome;
  usuario.value.idade = idade;
  usuario.value.dm = dm;
  usuario.value.estado = estado;
  usuario.value.cidade = cidade;
  usuario.value.endereco = endereco;
  usuario.value.hobbies = hobbies;
  usuario.value.lingProg = lingProg;
  usuario.value.bio = bio;
})


</script>

<template>


</template>

<style scoped></style>
