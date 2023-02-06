<script setup>
import Button from "@/components/Button.vue";
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
</template><img src="../../../OneDrive/Desktop/icon.png" height="189" width="294"/>

<style scoped>
header {
  line-height: 1.5;
}
main {
  overflow: hidden;
}
</style>
