<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <h1 class="text-3xl font-bold m-2">Hello world!</h1>

      <nav
        class="text-2xl m-2 bg-amber-100 w-3/12 flex justify-around align-middle dark:bg-slate-800 space-x-2"
      >
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <div class="m-2">
    <RouterView />
  </div>
</template>
