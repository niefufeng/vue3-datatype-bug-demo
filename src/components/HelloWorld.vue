<template>
  <div>
    <br />

    <div>
      <span>current value: </span>
      <span>{{ count }}</span>
    </div>

    <br />

    <div>
      <span>current value type: </span>
      <strong>{{ countType }}</strong>
    </div>

    <br />

    <select v-model="count">
      <option :value="1">1</option>
      <option :value="2">2</option>
      <option :value="3">3</option>
    </select>
  </div>
</template>

<script setup>
import { computed, reactive, ref } from 'vue'

const data = reactive({
  int: 1
});

const count = ref(1);

const countType = computed(() => typeof count.value);
</script>

<style scoped>
select {
  padding: 0.5em 2em;
}
</style>