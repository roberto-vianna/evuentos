<script setup>
import { ref } from "vue";

const nome = ref("");
const email = ref("");
const descricao = ref("");

function enviarEmail() {
  alert(
    "Nome:" + nome.value + "Email:" + email.value + "msg:" + descricao.value
  );
}
</script>

<template>
  <div class="columns">
    <div class="column">
      Formulario
      <input
        v-model="nome"
        class="input is-primary mb-3"
        type="text"
        placeholder="Nome"
      />
      <input
        v-model="email"
        class="input is-primary mb-3"
        type="email"
        placeholder="Email"
      />
      <textarea
        v-model="descricao"
        class="textarea is-primary mb-3"
        type="text"
        placeholder="Descrição"
        rows="10"
      ></textarea>
      <button class="button is-primary is-fullwidth" @click="enviarEmail()">
        Enviar
      </button>

      <p>Nome: {{ nome }}</p>
      <p>Email: {{ email }}</p>
      <p>Descrição: {{ descricao }}</p>
    </div>

    <div class="column">
      <img src="../assets/form.png" width="75%" />
    </div>
  </div>
</template>
