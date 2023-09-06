<script setup>
import { ref } from "vue";

const codeCumbersome = ref(`
`);
</script>

<template>
  <section class="relative">
    <img
      class="w-[20rem] absolute -top-5 -right-6"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997462/zuiw7o50cq3xzzqyeyi8.svg"
      alt="top"
    />
    <div class="absolute top-2 left-2 space-y-5">
      <h1 v-click class="text-gray-700 font-bold text-3xl">
        Problem Scenario:
      </h1>
      <div class="grid grid-cols-2 text-gray-600">
        <div class="space-y-2">
          <p v-click>
            When dealing with forms on the frontend, we often need to sync the
            state of form input elements with corresponding state in JavaScript.
          </p>
          <p v-click>
            It can be cumbersome to manually wire up value bindings and change
            event listeners:
          </p>
          <div v-html="codeCumbersome"></div>
        </div>
      </div>
    </div>
    <img
      class="w-[20rem] absolute top-[27rem] -left-5"
      src="https://res.cloudinary.com/montanasolutions/image/upload/v1693997461/gvlauyrg7lkmtkkaywib.svg"
      alt="bottom"
    />
  </section>
</template>
