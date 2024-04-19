<template>
  <div class="custom-container">
    <ExportProducts />
  </div>
</template>

<script>
import ExportProducts from './components/ExportProducts.vue';
export default {
  name: 'App',
  components: {
    ExportProducts
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