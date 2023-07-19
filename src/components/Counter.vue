<script setup lang="ts">
import { ref, onMounted } from 'vue';
import PrimaryButton from './PrimaryButton.vue';
import DangerButton from './DangerButton.vue';

let count = ref(0);
let resetCount  = ref(0);

</script>

<template>
  <p class="w-full mt-8 flex justify-center font-orbitron">Trenutno pripremamo narudžbu</p>
  <p class="w-full flex justify-center font-orbitron text-2xl">GASTRO WINGS:</p>
  <div class="flex justify-center">
    <span ref="counter" class="text-7xl font-bold text-red-600 font-orbitron">{{ count }}</span>
  </div>
  <div class="w-full mt-4 flex flex-row space-x-4 justify-center">
    <primary-button ref="incrementButton" title="+" @click="count++" class=" bg-green-600 text-xl" />
    <primary-button ref="decrementButton" title="-" @click="count--" />
    <input placeholder="0" class="border rounded w-12 mr-12"  onclick="this.focus();this.select()"   v-model="count" 
    type="number" >
    <danger-button ref="resetButton" class="ml-16" title="Reset" @click="count = 0" />
    
    
  </div>
  <div class="w-full mt-4 flex flex-row space-x-4 justify-center">
    
  </div>
</template>
