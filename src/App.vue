<script setup>
import { ref } from "vue";
import Tweet from "./components/Tweet.vue";
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";

const tweet = ref([
  {
    user: {
      name: "Thoughts of Dog®",
      image: "https://i.imgur.com/b0EdHVV.jpg",
      handle: "dog_feelings",
    },
    timestamp: "1h ago",
    message:
      "Humanity is the quality of being kind, thoughtful, and sympathetic towards others",
  },
  {
    user: {
      name: "Thoughts of Dog®",
      image: "https://i.imgur.com/b0EdHVV.jpg",
      handle: "dog_feelings",
    },
    timestamp: "2h ago",
    message: "The purpose of our lives is to be happy",
  },
  {
    user: {
      name: "Thoughts of Dog®",
      image: "https://i.imgur.com/b0EdHVV.jpg",
      handle: "dog_feelings",
    },
    timestamp: "3h ago",
    message:
      "Never let the fear of striking out keep you from playing the game",
  },
]);
</script>

<template>
  <div class="app">
    <Tweet
      v-for="(tweet, index) in tweets"
      :key="index"
      :messageFather="tweet.message"
      :timestampFather="tweet.timestamp"
      :userFather="tweet.user"
      :imageFather="tweet.user.image"
    />
  </div>
</template>

<style scoped></style>
