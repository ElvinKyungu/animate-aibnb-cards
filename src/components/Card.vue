<script setup lang="ts">
import { onMounted } from 'vue';
import gsap from 'gsap';

onMounted(() => {
  const images = document.querySelectorAll('.animate-img');
  const tl = gsap.timeline({ repeat: -1, repeatDelay: 1 });

  images.forEach((image, index) => {
    tl.fromTo(image,
      { 
        width: "0px", 
        height: "0px", 
        opacity: 0 
      },
      {
        width: "10rem",
        height: "10rem",
        opacity: 1,
        duration: .6,
        ease: "power4.out"
      }
    );
  });
});
</script>


<template>
  <main class="flex flex-wrap gap-4 -space-x-28 justify-start w-[26rem]">
    <img
      src="https://a0.muscache.com/im/pictures/hosting/Hosting-U3RheVN1cHBseUxpc3Rpbmc6MTEzMTg2NzMzNDc0MDk1Nzg4NA%3D%3D/original/b676fc8d-8250-4df0-a7cb-728b0486e371.jpeg?im_w=1440&im_q=highq" 
      alt=""
      class="animate-img transform rotate-12 object-cover rounded-2xl border-4 border-gray-100"
    >
    <img
      src="https://a0.muscache.com/im/pictures/hosting/Hosting-U3RheVN1cHBseUxpc3Rpbmc6MTEzMTg2NzMzNDc0MDk1Nzg4NA%3D%3D/original/b676fc8d-8250-4df0-a7cb-728b0486e371.jpeg?im_w=1440&im_q=highq" 
      alt=""
      class="animate-img transform -rotate-12 object-cover rounded-2xl border-4 border-gray-100"
    >
    <img
      src="https://a0.muscache.com/im/pictures/hosting/Hosting-U3RheVN1cHBseUxpc3Rpbmc6MTEzMTg2NzMzNDc0MDk1Nzg4NA%3D%3D/original/b676fc8d-8250-4df0-a7cb-728b0486e371.jpeg?im_w=1440&im_q=highq" 
      alt=""
      class="animate-img transform rotate-6 object-cover rounded-2xl border-4 border-gray-100"
    >
    <img
      src="https://a0.muscache.com/im/pictures/hosting/Hosting-U3RheVN1cHBseUxpc3Rpbmc6MTEzMTg2NzMzNDc0MDk1Nzg4NA%3D%3D/original/b676fc8d-8250-4df0-a7cb-728b0486e371.jpeg?im_w=1440&im_q=highq" 
      alt=""
      class="animate-img transform -rotate-12 object-cover rounded-2xl border-4 border-gray-100"
    >
    <img
      src="https://a0.muscache.com/im/pictures/hosting/Hosting-U3RheVN1cHBseUxpc3Rpbmc6MTEzMTg2NzMzNDc0MDk1Nzg4NA%3D%3D/original/b676fc8d-8250-4df0-a7cb-728b0486e371.jpeg?im_w=1440&im_q=highq" 
      alt=""
      class="animate-img transform object-cover rounded-2xl border-4 border-gray-100"
    >
  </main>
</template>

<style>
</style>
