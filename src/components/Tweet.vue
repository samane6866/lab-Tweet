<template>
  <div className="tweet">
    <ProfileImage
      :image="imageFather"
      :imageAlt="`${userFather.name} - profile image`"
    />
    <!-- Bypassing the use of a component to extract logic and inyecting the object user.image through the prop userFather -->

    <!-- <img :src="userFather.image" className="profile" :alt="imageAlt" /> -->

    <div class="body">
      <!-- Iteration 1 - preRefactoring -->
      <!-- <div class="top">
        <User :user="userFather" />
        <Timestamp :timestamp="timestampFather" />
      </div> -->

      <!-- Iteration 2 - postRefactoring -->
      <div class="top">
        <User :user="userFather" :timestamp="timestampFather" />
      </div>
      <Message v-bind:message="messageFather" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script setup>
import Message from "./Message.vue";
import user from "./user.vue";
import ProfileImage from "./ProfileImage.vue";
import Timestamp from "./Timestamp.vue";

defineProps({
  message: {
    type: string,
  },

  timestamp: {
    type: string,
  },

  user: {
    type: object,
  },

  image: {
    type: string,
  },

  imageAlt: {
    type: string,
  },
});
</script>

<style scoped></style>
