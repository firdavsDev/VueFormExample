<template>
  <div class="custom-container">
    <ExportProducts />
  </div>
</template>

<script>
import ExportProducts from './components/ExportProducts.vue';
import { inject } from '@vercel/analytics';
export default {
  name: 'App',
  components: {
    ExportProducts
  },
  setup() {
    inject();
  }
}
</script>
<style>
.custom-container {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>