<script setup>
import HeartButtonJson from "~/assets/lottie/heart-button.json";

const lottieAnimation = ref(null);
</script>

<template>
  <ClientOnly>
    <Vue3Lottie
      ref="lottieAnimation"
      :animationData="HeartButtonJson"
      :width="100"
      :height="100"
      :play-on-hover="true"
    />
  </ClientOnly>
</template>
