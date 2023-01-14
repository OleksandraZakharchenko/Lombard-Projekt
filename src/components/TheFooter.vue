<template>
  <footer class="footer">
    <BaseDivider />
    <BaseHeading variant="h1" class="footer__title">Lombard</BaseHeading>
  </footer>
</template>

<script setup>
import BaseHeading from "./UI/BaseHeading.vue";
import BaseDivider from "@/components/UI/BaseDivider.vue";
</script>

<style scoped>
.footer__title {
  display: flex;
  justify-content: center;
  align-items: center;
  color: #398000;
  justify-self: center;
  align-self: center;
  height: 100%;
}
</style>
