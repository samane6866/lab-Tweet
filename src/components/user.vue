<template>
  <div class="top">
    <span className="name">{{ user.name }}</span>
    <span className="handle">{{ user.handle }}</span>
    <Timestamp v-bind:timestamp="timestamp" />
  </div>
</template>

<script setup>
import { stringify } from "postcss";

defineProps({
  user: {
    type: Object,
    default: () => ({
      name: "Arian",
      handel: "@Arian",
    }),
  },

  Timestamp: {
    type: String,
  },
});
</script>

<style scoped></style>
