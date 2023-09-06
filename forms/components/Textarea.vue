<script setup>
import { ref } from 'vue'

const text = ref('')
</script>

<template>
    <div class="max-w-sm">
        <p>Output: {{ text }}</p>
        <textarea v-model="text" cols="30" rows="4" class="border rounded-md p-2 text-gray-600 placeholder:text-gray-600" placeholder="edit me"></textarea>
    </div>
</template>
