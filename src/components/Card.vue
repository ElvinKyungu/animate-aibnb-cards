<script setup lang="ts">
import { ref, onMounted } from 'vue';
import gsap from 'gsap';

const imgUrl = ref("https://a0.muscache.com/im/pictures/hosting/Hosting-U3RheVN1cHBseUxpc3Rpbmc6MTEzMTg2NzMzNDc0MDk1Nzg4NA%3D%3D/original/b676fc8d-8250-4df0-a7cb-728b0486e371.jpeg?im_w=1440&im_q=highq");

onMounted(() => {
  const images = document.querySelectorAll('.animate-img');
  const tl = gsap.timeline({ repeat: -1, repeatDelay: .1 });

  tl.fromTo(images,
    { 
      scale: 0,
      opacity: 0 
    },
    {
      scale: 1,
      opacity: 1,
      duration: .9,
      ease:"elastic.out(0.4,0.4)",
      stagger: {
        each: 0.06,
      }
    }
  )
})
</script>

<template>
  <div class="flex flex-wrap gap-4 -space-x-24 justify-start w-[32rem] m-auto">
    <img
      :src="imgUrl" 
      alt=""
      class="animate-img image-animate rotate-12"
    >
    <img
      :src="imgUrl"
      alt=""
      class="animate-img image-animate -rotate-12"
    >
    <img
      :src="imgUrl"
      alt=""
      class="animate-img image-animate rotate-6"
    >
    <img
      :src="imgUrl"
      alt=""
      class="animate-img image-animate -rotate-12"
    >
    <img
      :src="imgUrl"
      alt=""
      class="animate-img image-animate object-cover"
    >
  </div>
</template>

<style>
</style>
