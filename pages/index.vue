<template>
  <div>
    <Tutorial />

  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Tutorial from '@/components/Tutorial.vue';

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Tutorial,
  },
});
</script>

<style scoped>
/* Adicione o estilo necessário aqui */
</style>
