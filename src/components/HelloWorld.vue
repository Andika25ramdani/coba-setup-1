<script setup lang="ts">
defineProps<{ msg: string }>()

const count = ref(0)
const dateModel = ref()
</script>

<template>
  <h1 class="bg-red-500">{{ msg }}</h1>

  <div class="card">
    <el-button type="primary">El-Button</el-button>
    <el-date-picker v-model="dateModel" type="daterange" />
    <button type="button" @click="count++" class="outlined-button">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Learn more about IDE Support for Vue in the
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Vue Docs Scaling up Guide</a
    >.
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
