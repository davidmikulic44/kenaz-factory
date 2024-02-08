<script setup>
import Sidebar from "../Sidebar/Sidebar.vue";
import Banner from "../Banner/Banner.vue";
import CategoryArticles from "./CategoryArticles.vue";
</script>

<template>
  <div class="feed-container">
    <div class="main-column">
      <CategoryArticles></CategoryArticles>
      <Banner size="mid"></Banner>
    </div>
    <aside class="side-column">
      <Sidebar></Sidebar>
    </aside>
  </div>
</template>
