<template>
  <div>
    <Tutorial />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Tutorial from '@/components/Tutorial.vue';

export default defineComponent({
  name: 'IndexPage',
  components: {
    Tutorial,
  },
});
</script>


