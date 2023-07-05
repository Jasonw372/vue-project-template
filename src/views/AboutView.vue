<script lang="ts" setup>
import { useDark, useToggle } from '@vueuse/core'

const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<template>
  <div class="flex space-x-4">
    <span @click.stop="toggleDark()">暗黑模式</span>

    <el-switch size="small" v-model="isDark" />
  </div>
</template>
