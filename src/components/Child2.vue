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
  <div class="child2">
    <h2>Child2: Consumer</h2>
    <p>count: {{ count }}</p>
  </div>
</template>

<style scoped>
.child2 {
  border: 1px solid green;
}
</style>