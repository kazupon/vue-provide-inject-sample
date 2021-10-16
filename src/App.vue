<script setup lang="ts">
import Parent1 from './components/Parent1.vue'
import Parent2 from './components/Parent2.vue'
import { ref } from 'vue'

const hide = ref(true)
</script>

<template>
  <div class="root">
    <h1>Root</h1>
    <form>
      <label>
        <input type="checkbox" v-model="hide" />
        Hide Parent1
      </label>
    </form>
    <div class="container">
      <Parent1 v-if="hide" />
      <Parent2 />
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<style scoped>
.root {
  border: 3px solid green;
}
.container {
  display: flex;
  flex-direction: row;
}
</style>