<script setup>
import { ref } from "vue";

const selected = ref([]);
</script>

<template>
  <div>
    <div>Selected: {{ selected }}</div>

    <select v-model="selected" multiple class="w-sm">
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </div>
</template>
