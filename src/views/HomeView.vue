<script setup lang="ts">
import ArticleItem from '@components/article/article-item.vue';
</script>

<template>
  <main class="main">
    <ArticleItem></ArticleItem>
    <ArticleItem></ArticleItem>
    <ArticleItem></ArticleItem>
    <ArticleItem></ArticleItem>
    <ArticleItem></ArticleItem>
  </main>
</template>

<style lang="scss">
.main {
  @include flex(flex-start, center, column);
  padding: 20px;
}
</style>
