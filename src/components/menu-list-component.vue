<script setup lang="ts">
const isCollapse = ref(false)
</script>
<template>
  <el-aside class="bg-red-50">
    <el-menu :collapse="isCollapse" class="bg-orange-50">
      <el-button @click="isCollapse = !isCollapse" class="hidden md:block">Toggle</el-button>
      <el-menu-item v-for="i in 8" :index="`${i}`" :key="i">
        <template #title>Navigator {{ i }}</template>
      </el-menu-item>
    </el-menu>
  </el-aside>
</template>
<style scoped>
.aes-aside {
  @apply w-max;
}

.aes-menu--vertical {
  @apply fixed sm:relative;
  @apply h-screen;
  @apply w-screen sm:w-20;
  @apply overflow-x-hidden;

  &:not(.aes-menu--collapse) {
    @apply w-screen sm:w-72;
  }
}
</style>
