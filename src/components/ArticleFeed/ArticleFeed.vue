<script setup>
import "./styles/_articleFeed.scss";
import ArticleHeader from "./ArticleHeader.vue";
import Sidebar from "../Sidebar/Sidebar.vue";
import Article from "./Article.vue";
import Banner from "../Banner/Banner.vue";
import AuthorAbout from "./AuthorAbout.vue";
import Comments from "./Comments.vue";
</script>

<template>
  <ArticleHeader></ArticleHeader>
  <div class="feed-container">
    <div class="main-column">
      <Article></Article>
      <Banner size="mid"></Banner>
      <AuthorAbout></AuthorAbout>
      <Comments></Comments>
    </div>
    <aside class="side-column">
      <Sidebar></Sidebar>
    </aside>
  </div>
</template>
