<template>
  <div class="label">
    <component :is="component"></component>
  </div>
</template>

<script setup lang="ts">
import LabelNormal from './label-normal.vue';
import LabelToDo from './label-todo.vue';

const props = withDefaults(
  defineProps<{
    type?: string;
  }>(),
  {
    type: 'normal',
  }
);
const component = props.type === 'normal' ? LabelNormal : LabelToDo;
</script>

<style lang="scss" scoped>
.label {
  margin-right: 10px;
}
</style>
