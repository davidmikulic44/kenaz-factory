<script setup>
import Header from "@/components/Header/Header.vue";
import Footer from "@/components/Footer/Footer.vue";
import Categories from "@/components/Header/Categories.vue";
import Banner from "@/components/Banner/Banner.vue";
import ArticleCarousel from "@/components/ArticleCarousel/ArticleCarousel.vue";
import CategoryFeed from "@/components/CategoryFeed/CategoryFeed.vue";
</script>

<template>
  <Header></Header>
  <Categories></Categories>
  <Banner size="big"></Banner>
  <ArticleCarousel></ArticleCarousel>
  <CategoryFeed></CategoryFeed>
  <Footer></Footer>
</template>
