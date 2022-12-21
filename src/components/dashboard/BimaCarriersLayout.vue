<template>
  <div class="bima-main-layout">
    <bima-carriers-header />
    <router-view />
    <bima-carriers-footer />
  </div>
</template>
<script>
import BimaCarriersHeader from "./BimaCarriersHeader.vue";
import BimaCarriersFooter from "./BimaCarriersFooter.vue";
export default {
  name: "main-layout",
  components: { BimaCarriersHeader, BimaCarriersFooter },
};
</script>
