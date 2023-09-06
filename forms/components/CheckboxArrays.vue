<script setup>
import { ref } from "vue";

const checkedNames = ref([]);
</script>

<template>
  <div>
    <div>Checked names: {{ checkedNames }}</div>
    <div class="flex gap-3">
        <div class="space-x-2">
          <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
          <label for="jack">Jack</label>
        </div>

        <div class="space-x-2">
          <input type="checkbox" id="john" value="John" v-model="checkedNames" />
          <label for="john">John</label>
        </div>

        <div class="space-x-2">
          <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
          <label for="mike">Mike</label>
        </div>
    </div>
  </div>
</template>
