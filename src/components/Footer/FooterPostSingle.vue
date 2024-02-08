<script setup>
const props = defineProps(["date", "readTime", "title"]);
</script>

<template>
  <article class="footer-single-post">
    <div class="footer-post-desc">
      <div class="footer-post-header">
        <h6 class="footer-post-info">
          {{ date }}
        </h6>
        <h6 class="footer-post-info">
          {{ readTime }}
        </h6>
      </div>
      <router-link to="/article">
        <h3 class="footer-post-title">
          {{ title }}
        </h3>
      </router-link>
    </div>
    <div class="post-container">
      <img
        src="../../assets/manofsteel.jpeg"
        class="footer-post-image"
        alt=""
      />
    </div>
  </article>
</template>
