<script setup>
import { ref } from "vue";
import TweetSingle from "./TweetSingle.vue";

const tweets = ref([
  {
    author: "Envato @envato",
    text: "Is this your typical million dollar day in the park? http://enva.to/150vxFC  Happy @TrueThemes Day! #ThemeForest pic.twitter.com/EHz7awxOXy",
  },
  {
    author: "Envato @envato",
    text: "Is this your typical million dollar day in the park? http://enva.to/150vxFC  Happy @TrueThemes Day! #ThemeForest pic.twitter.com/EHz7awxOXy",
  },
  {
    author: "Envato @envato",
    text: "Is this your typical million dollar day in the park? http://enva.to/150vxFC  Happy @TrueThemes Day! #ThemeForest pic.twitter.com/EHz7awxOXy",
  },
]);
</script>

<template>
  <section class="footer-tweets">
    <h1 class="footer-posts-title">Twitter feed</h1>
    <TweetSingle
      v-for="(tweet, index) in tweets"
      :key="index"
      :author="tweet.author"
      :text="tweet.text"
    >
    </TweetSingle>
  </section>
</template>
