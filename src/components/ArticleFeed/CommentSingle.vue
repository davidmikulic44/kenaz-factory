<script setup>
const props = defineProps(['name', 'comment', 'time']);

const formatTimestamp = (timestamp) => {
  const options = { 
    year: 'numeric', 
    month: 'long', 
    day: 'numeric', 
    hour: 'numeric', 
    minute: 'numeric' 
  };
  return new Date(timestamp).toLocaleDateString('en-US', options);
};
</script>

<template>
  <div class="comment-container-outer">
    <img src="../../assets/commentpfp.png" class="comment-pfp">
    <div class="comment-container">
    <div class="comment-header">
      <div class="comment-info">
        <h3 class="comment-author">{{ name }}</h3>
        <h6 class="comment-timestamp">{{ formatTimestamp(time) }}</h6>
      </div>
      <button class="reply-button">Reply</button>
    </div>
    <p class="article-text">{{ comment }}</p>
  </div>
  </div>
</template>
