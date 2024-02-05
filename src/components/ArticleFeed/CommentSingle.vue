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
  <div>
    <img src="../../assets/commentpfp.png" alt="">
    <div class="comment-header">
      <div class="comment-info">
        <h3>{{ name }}</h3>
        <h6>{{ formatTimestamp(time) }}</h6>
      </div>
      <button>Reply</button>
    </div>
    <p>{{ comment }}</p>
  </div>
</template>
