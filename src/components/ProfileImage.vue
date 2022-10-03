<template>
  <img :src="image" className="profile" :alt="imageAlt" />
</template>

<script set up>
defineProps({
  image: {
    type: string,
    default: "https://i.imgur.com/b0EdHVV.jpg",
  },

  imageAlt: {
    type: string,
  },
});
</script>

<style></style>
