<template>
  <div class="container">
    <component-header />
    <div class="content">
      <nuxt />
    </div>
    <component-footer />
  </div>
</template>
<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    "component-header": Header,
    "component-footer": Footer,
  },
};
</script>
<style scoped>
.content {
  padding-top: 63px;
}
</style>
