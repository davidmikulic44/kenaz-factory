<script setup>
import CategorySingleArticle from "./CategorySingleArticle.vue";
import CategoryPagination from "./CategoryPagination.vue";
import "./styles/_categoryFeed.scss";
</script>

<template>
  <div class="category-feed-container">
    <div class="category-title-container">
      <h1 class="category-title">News</h1>
    </div>
    <CategorySingleArticle></CategorySingleArticle>
    <CategorySingleArticle></CategorySingleArticle>
    <CategorySingleArticle></CategorySingleArticle>
    <CategorySingleArticle></CategorySingleArticle>
    <CategorySingleArticle></CategorySingleArticle>
    <CategorySingleArticle></CategorySingleArticle>
    <CategoryPagination></CategoryPagination>
  </div>
</template>
