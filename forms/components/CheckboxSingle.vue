<script setup>
import { ref } from 'vue'

const checked = ref(false)
</script>

<template>
  <div class="space-x-2">
    <input type="checkbox" id="checkbox" v-model="checked" />
    <label for="checkbox">{{ checked }}</label>
  </div>
</template>
