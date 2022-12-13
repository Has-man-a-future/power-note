<template>
  <div class="header">
    <nav class="menu">
      <router-link to="/">首页</router-link>
      <router-link to="category">分类</router-link>
      <router-link to="label">标签</router-link>
    </nav>
    <h1 class="title">Power Note</h1>
  </div>
</template>

<script setup lang="ts">
import { RouterLink } from "vue-router";
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 400px;
  background: $b-main;
  padding: 20px;
  @include flex(center, center, column);
  .menu {
    @include flex(flex-end, center);
    column-gap: 8px;
    align-self: flex-end;
  }
  .title {
    flex: 1;
    font-size: 48px;
    font-weight: 600;
    text-align: center;
    color: $c-main;
    @include flex(center, center);
  }
}
</style>
