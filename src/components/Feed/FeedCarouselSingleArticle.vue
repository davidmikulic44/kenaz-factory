<script setup>
const props = defineProps(["size"]);
</script>

<template>
  <article class="feed-single-article" :class="size">
    <img
      src="../../assets/banner.jpg"
      class="feed-article-image"
      :class="size + '-image'"
    />
    <div class="footer-post-header">
      <h6 class="footer-post-info">January 19, 2024</h6>
      <h6 class="footer-post-info">20</h6>
    </div>
    <h3 class="feed-article-title">
      <router-link to="/article">
        For Obama, MLK's shadow looms large ahead of speech
      </router-link>
    </h3>
  </article>
</template>
