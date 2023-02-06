<script setup>
import Header from "@/components/Header.vue";
import Calculator from "@/components/Calculator.vue";
</script>

<template>
  <header>
    <Header></Header>
  </header>

  <main ref="main">
      <Calculator></Calculator>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}
main {
  overflow: hidden;
}
</style>
