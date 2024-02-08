<script setup>
const props = defineProps(["category", "numArticles"]);
const generateArticleArray = () => {
  return new Array(Number(props.numArticles)).fill(null);
};
</script>

<template>
  <section class="feed-single-section" :class="category">
    <div class="feed-header">
      <h1 class="feed-title">{{ category }}</h1>
      <router-link to="/category" class="feed-read-all">See all</router-link>
    </div>
    <section :class="'feed-articles' + numArticles">
      <article
        v-for="index in generateArticleArray()"
        :key="index"
        :class="'feed-single-article' + numArticles"
      >
        <img src="../../assets/banner.jpg" class="feed-article-image" />
        <div class="feed-article-info-container">
          <div class="feed-post-header">
            <h6 class="feed-post-info">January 19, 2024</h6>
            <h6 class="feed-post-info">20</h6>
          </div>
          <router-link to="/article"
            ><h3 class="feed-article-title">
              For Obama, MLK's shadow looms large ahead of speech
            </h3>
          </router-link>
        </div>
      </article>
    </section>
  </section>
</template>
