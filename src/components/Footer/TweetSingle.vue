<script setup>
const props = defineProps(["author", "text"]);
</script>

<template>
  <div class="single-tweet">
    <div class="tweet-header">
      <img src="../../assets/tweet-icon.svg" />
      <h3 class="tweet-author">{{ author }}</h3>
    </div>
    <p class="tweet-content">{{ text }}</p>
  </div>
</template>
