<script setup>
import { ref } from "vue";

const picked = ref("");
</script>

<template>
  <div>
    <div>Picked: {{ picked }}</div>

    <div class="flex gap-2">
      <div class="space-x-1">
        <input type="radio" id="one" value="One" v-model="picked" />
        <label for="one">One</label>
      </div>
      <div class="space-x-1">
        <input type="radio" id="two" value="Two" v-model="picked" />
        <label for="two">Two</label>
      </div>
    </div>
  </div>
</template>
