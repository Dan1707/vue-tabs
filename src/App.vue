<script setup>
import TabsWrapper from "./components/TabsWrapper.vue";
import TabsNav from "./components/TabsNav.vue";
</script>

<template>
  <div class="wrapper">
    <h1>Tabs on Vue 3 setup</h1>

    <TabsWrapper />
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  background-color: #3a3a3a;
  color: #ffffff;
  width: 100%;
  height: 100vh;
  text-align: center;
}
</style>
