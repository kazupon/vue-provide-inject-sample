<script setup lang="ts">
import Child2 from './Child2.vue'
</script>

<template>
  <div class="parent2">
    <h2>Parent2</h2>
    <Child2 />
  </div>
</template>

<style scoped>
.parent2 {
  border: 2px solid blue;
  width: 50%;
}
</style>