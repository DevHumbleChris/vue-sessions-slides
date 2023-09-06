<script setup>
import { ref } from "vue";

const message = ref("");
</script>

<template>
  <div>
    <p>Message is: {{ message }}</p>
    <input
      type="text"
      v-model="message"
      class="border rounded-md p-2 text-gray-600 placeholder:text-gray-600"
      placeholder="edit me"
    />
  </div>
</template>
