<script setup lang="ts">
import { onMounted, ref } from "vue";
import HeartButtonJson from "~/assets/lottie/heart-button.json";

const isOpening = ref(true);
const durationMs = 3000;

onMounted(() => {
  setTimeout(() => {
    isOpening.value = false;
  }, durationMs);
});
</script>

<template>
  <transition>
    <OpeningAnimation v-if="isOpening" />
    <main v-else>
      <h1>Home</h1>

      <LikeButton @click="() => {}" />
    </main>
  </transition>
</template>

<style scoped>
.v-enter-from,
.v-leave-to {
  opacity: 0;
}
.v-enter-to,
.v-leave-from {
  opacity: 1;
}
.v-enter-active,
.v-leave-active {
  transition: opacity 1s ease-in-out;
}
</style>
