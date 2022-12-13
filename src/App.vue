<script setup lang="ts">
import { RouterView } from "vue-router";
import Header from "@components/layout/layout-header.vue";
</script>

<template>
  <Header></Header>
  <main>
    <RouterView />
  </main>
</template>

<style scoped></style>
