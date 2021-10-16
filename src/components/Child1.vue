<script setup lang="ts">
import { Key1 } from '../keys'
import { ref, inject, watchEffect } from 'vue'
import type { Ref } from 'vue'

const count = inject<Ref<number>>(Key1, ref(0))

watchEffect(() => {
  console.log('count', count.value)
})
</script>

<template>
  <div class="child1">
    <h2>Child1</h2>
    <p>count: {{ count }}</p>
  </div>
</template>

<style scoped>
.child1 {
  border: 1px solid blue;
}
</style>