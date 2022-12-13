<template>
  <div class="article-item">
    <div class="title-content">
      <LabelIndex></LabelIndex>
      <p class="title" cursor>{{ article.title }}</p>
    </div>
    <div class="timer">
      <i class="iconfont pn-rili"></i>{{ article.created_at }}0
    </div>
    <p class="description">{{ article.description }}</p>
    <div class="labels">
      <el-tag
        cursor
        @click="toLabel(item.id)"
        v-for="item in article.tags"
        :key="item.id"
        class="ml-2"
        >{{ item.name }}</el-tag
      >
    </div>
  </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";
import LabelIndex from "@components/common/label/label-index.vue";
import { useRouter } from "vue-router";
const router = useRouter();

const article = reactive({
  title: "About Power Note - How to use power note?",
  created_at: "2022-12-13 10:54:00",
  tags: [
    {
      id: "0001",
      name: "入门",
    },
  ],
  description:
    "This Note tell you how to use power note in your work job or study .....",
});

const toLabel = (lableId: string) => {
  router.push(lableId);
};
</script>

<style lang="scss" scoped>
.article-item {
  width: 70vw;
  max-height: 400px;
  min-height: 180px;
  border-bottom: 3px dashed rgba($c-second, 0.3);
  & + & {
    margin-top: 30px;
  }
  .title-content {
    @include flex(flex-start, center);
    .title {
      font-size: 28px;
      color: $c-second;
      &:hover {
        color: $b-main;
        text-decoration: underline;
      }
    }
  }

  .timer {
    margin-top: 20px;
    font-size: 12px;
    color: $c-info;
  }
  .description {
    margin-top: 20px;
    @include ellipsis-mult(3);
    color: $c-desc;
  }
  .labels {
    margin-top: 20px;
  }
}
</style>
