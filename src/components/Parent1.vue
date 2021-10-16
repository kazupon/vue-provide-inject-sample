<script setup lang="ts">
import Child1 from './Child1.vue'
import { Key1 } from '../keys'
import { ref, provide } from 'vue'
import type { Ref } from 'vue'

const count = ref(0)
provide<Ref<number> >(Key1, count)
</script>

<template>
  <div class="parent1">
    <h2>Parent1: Provider</h2>
    <p>count: {{ count }}</p>
    <button @click="count++">click</button>
    <Child1 />
  </div>
</template>

<style scoped>
.parent1 {
  border: 2px solid red;
  width: 50%;
}
</style>