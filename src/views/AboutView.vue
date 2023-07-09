<script lang="ts" setup>
import { useDark, useToggle } from '@vueuse/core'
import { WebviewWindow } from '@tauri-apps/api/window';

const isDark = useDark()
const toggleDark = useToggle(isDark)

const  create = function () {
  let webview = new WebviewWindow('theUniqueLabel', {
    url: 'https://github.com/tauri-apps/tauri'
  });

  webview.once('tauri://created', function () {
    webview.setTitle("")
    webview.setSkipTaskbar(false)
  });
}

</script>

<template>
  <div class="flex space-x-4">
    <span @click.stop="toggleDark()">暗黑模式</span>

    <el-switch size="small" v-model="isDark" />

    <el-button type="primary" size="small" @click="create">点我出窗口</el-button>
  </div>
</template>
