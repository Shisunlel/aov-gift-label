<template>
  <div class="w-full h-full flex justify-center items-center">
    <div>
      <div class="w-full max-w-2xl p-4 rounded bg-red-400 text-white">
        <div class="border-2 rounded flex flex-col md:flex-row md:items-center md:gap-8 p-4">
          <img src="/assets/santa.svg" alt="" class="max-w-[12em]" />
          <div>
            <h1 class="font-serif text-4xl">Happy Holidays!</h1>
            <div class="mt-4 bg-white text-black p-2 rounded">TO: {{ message.to }}</div>
            <div class="mt-2 bg-white text-black p-2 rounded">FROM: {{ message.from }}</div>
          </div>
        </div>
      </div>
      <div class="flex flex-col py-4">
        <label for="To">To:</label>
        <input class="w-full rounded shadow p-2 border" type="text" id="To" v-model="message.to">
      </div>
      <div class="flex flex-col py-4">
        <label for="From">From:</label>
        <input class="w-full rounded shadow p-2 border" type="text" id="From" v-model="message.from">
      </div>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue';

const message = reactive({
  to: '',
  from: ''
})
</script>
