<script setup lang="ts">
const { x, y } = useMouse();
</script>

<template>
  <h1 class="text-red-300">Index page</h1>
  <NuxtImg src="https://placehold.co/600x400" />
  <Button>Test</Button>
  <Icon size="30px" name="uil:github" style="color: black" />
  <div>pos: {{ x }}, {{ y }}</div>
  <div>
    <NuxtLink href="/about">about</NuxtLink>
  </div>
</template>
