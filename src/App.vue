<template>
  <button @click="toggle">Toggle</button>
  <HelloWorld v-if="visible" />
</template>

<script setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

const visible = ref(true);

function toggle() {
  visible.value = !visible.value;
}
</script>

<style>
button {
  padding: 1em 2em;
  cursor: pointer;
}
</style>