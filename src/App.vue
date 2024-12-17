<script setup lang="ts">
import id from "element-plus/es/locale/lang/id"

import HelloWorld from "~component/HelloWorld.vue"
import MenuListComponent from "~component/menu-list-component.vue"
</script>

<template>
  <el-config-provider :locale="id" namespace="aes">
    <el-container class="h-screen">
      <menu-list-component />
      <el-container>
        <el-header>Header</el-header>
        <el-main>
          <HelloWorld msg="Vite + Vue" />
        </el-main>
        <el-footer>Footer</el-footer>
      </el-container>
    </el-container>
  </el-config-provider>
</template>
