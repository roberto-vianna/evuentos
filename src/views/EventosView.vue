<script setup>
import CardEventos from "@/components/CardEventos.vue";
import { computed, ref } from "vue";
const eventos = [
  { nome: "Minicurso Vue 3", local: "youtube Zona dev", data: "10/02/2024" },
  { nome: "Minicurso Vue 2", local: "youtube Zona dev", data: "22/02/2024" },
  { nome: "JS na Prática", local: "youtube Guanabara", data: "18/02/2024" },
  { nome: "Typescript", local: "youtube Dev master", data: "03/02/2024" },
];

const nome = ref("");
const eventosFiltrados = computed(() => {
  const filtro = nome.value.toLocaleLowerCase();
  return eventos.filter(
    (evento) =>
      evento.nome.toLocaleLowerCase().includes(filtro) ||
      evento.data.toLocaleLowerCase().includes(filtro) ||
      evento.local.toLocaleLowerCase().includes(filtro)
  );
});
</script>

<template>
  <input
    v-model="nome"
    class="input is-primary my-3"
    type="text"
    placeholder="Digite o nome do evento"
  />
  <div class="columns is-multiline mt-5">
    <CardEventos
      v-for="evento in eventosFiltrados"
      :key="evento.nome"
      :eventoRecebido="evento"
    />
  </div>
</template>
