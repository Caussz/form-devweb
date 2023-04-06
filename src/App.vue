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

  <main class="container">
    <h2>Form DevWeb</h2>

    <form> 
        <div class="input-field">
            <input type="text" placeholder="Seu nome">
            <div class="underline"></div>
        </div>
        <br>
        <div class="input-field">
            <input type="number" placeholder="Sua idade">
            <div class="underline"></div>
        </div>
        <input type="submit" value="Cadastrar info">
        <br>
    </form>

   
</main>


</template>

<style scoped>
  main.container {
  background: rgba(194, 176, 176, 0.815);
  min-width: 320px;
  min-height: 40vh;
  padding: 2rem;
  box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.2);
  border-radius: 8px;
  }
  
  main h2 {
  font-weight: 600;
  margin-bottom: 2rem;
  position: relative;
  }
  
  form {
  display: flex;
  flex-direction: column;
  }
  
  .input-field {
  margin: 10px;
  padding: 10px;
  background-color: transparent;
  position: relative;
  }
  
  form .input-field:first-child {
  margin-bottom: 1.5rem;
  }
  
  .input-field .underline::before {
  content: '';
  position: absolute;
  height: 1px;
  width: 100%;
  bottom: -5px;
  left: 0;
  background: rgba(0, 0, 0, 0.2);
  }
  
  .input-field .underline::after {
  content: '';
  position: absolute;
  height: 1px;
  width: 100%;
  bottom: -5px;
  left: 0;
  background: linear-gradient(45deg, #333135, #000000);
  transform: scaleX(0);
  transition: all .3s ease-in-out;
  transform-origin: left;
  }
  
  .input-field input:focus ~ .underline::after {
  transform: scaleX(1);
  }
  
  .input-field input {
  background-color: transparent;
  outline: none;
  font-size: 0.9rem;
  color: rgba(0, 0, 0, 0.7);
  width: 100%;
  }
  
  .input-field input::placeholder {
  color: rgba(0, 0, 0, 0.5);
  }
  
  form input[type="submit"] {
  margin-top: 2rem;
  padding: 0.4rem;
  width: 100%;
background-color: rgb(111, 86, 116);;
  cursor: pointer;
  color: white;
  font-size: 0.9rem;
  font-weight: 300;
  border-radius: 4px;
  transition: all 0.3s ease;
  }
  
  form input[type="submit"]:hover {
  transition: 5ms;
  letter-spacing: 0.5px;
  background: linear-gradient(to right, #5f6675, #537075);
  }

</style>
