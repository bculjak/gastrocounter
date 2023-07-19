<script setup lang="ts">
import { ref } from 'vue';
import PrimaryButton from './PrimaryButton.vue';
import DangerButton from './DangerButton.vue';

const count = ref(0);
</script>

<template>
    <p class="w-full mt-8 flex justify-center font-orbitron">Limited edition</p>
  <p class="w-full flex justify-center font-orbitron text-2xl">BEEFSTEAK TORTILJA:</p>
  <div class="flex justify-center">
    <span ref="counter" class="text-5xl font-bold text-red-600 font-orbitron">{{ count }} / 30</span>
  </div>
  <div class="w-full mt-4 flex flex-row space-x-4 justify-center">
    <primary-button ref="incrementButton" title="+" @click="count++" class=" bg-green-600 text-xl" />
    <primary-button ref="decrementButton" title="-" @click="count--" />
    <danger-button ref="resetButton" class="mr-8" title="Reset" @click="count = 0" />


  </div>

</template>
