<template>
  <div>
    <Tutorial />
    <Conta /> <!-- Adicione esta linha para incluir a tela de Conta -->
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Tutorial from '@/components/Tutorial.vue'; // Importando o componente Tutorial
import Conta from '@/pages/Conta.vue'; // Certifique-se de que o caminho esteja correto

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Tutorial,
    Conta, // Registre o componente Conta aqui
  },
});
</script>

<style scoped>
/* Adicione estilos específicos para esta página, se necessário */
</style>
