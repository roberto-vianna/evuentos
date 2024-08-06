<script setup>
defineProps({
  eventoRecebido: Object,
  nome: String,
  idade: Number,
});
</script>

<template>
  <div class="column is-3">
    <div class="card">
      <div class="card-content">
        <div class="media">
          <div class="media-content">
            <p class="title is-4">{{ eventoRecebido.nome }}</p>
            <p class="subtitle is-6">{{ eventoRecebido.local }}</p>
          </div>
        </div>

        <div class="content">
          {{ eventoRecebido.data }}
        </div>
      </div>
    </div>
  </div>
</template>
