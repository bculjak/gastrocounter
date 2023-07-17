<script setup lang="ts">
import Counter from './components/Counter.vue';
import Counter2 from './components/Counter2.vue';
</script>

<template>
  <div class="flex flex-row justify-around w-full">
    <div class=" bg-gray-900 h-screen w-full justify-evenly">
      <img src="./assets/logo.svg" width="200" class="m-auto mt-32"/>
      <img src="./assets/logo.svg" width="200" class="m-auto mt-32"/>
    </div>
    
    <div class=" w-full">
    <Counter />
  <Counter2 />
</div>
<div class=" bg-gray-900 h-screen w-full justify-evenly">
      <img src="./assets/logo.svg" width="200" class="m-auto mt-32"/>
      <img src="./assets/logo.svg" width="200" class="m-auto mt-32"/>
    </div>
  </div>

</template>
