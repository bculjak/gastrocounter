<script setup lang="ts">
import { ref, onMounted, onActivated } from 'vue';

const video = ref<HTMLVideoElement>();

// on component mounted callback
onMounted(async () => {
  // setup the video configuration
  await setupVideo(video);

  // auto play the video!
  video.value.play();
});

// configure the video element
async function setupVideo(video: HTMLVideoElement) {
  video.value.width = 640;
  video.value.height = 320;
  video.value.allowfullscreen = true;
  video.value.controls = true;
  video.value.type = 'video/webm';
  video.value.src =
    'https://cdn.glitch.global/0efdddf2-4a7a-4b65-b402-9e0fa8ff9db1/flower.webm?v=1648373099268';
}
</script>

<template>
  <video ref="video" />
</template>
