<script>
import Header from "@/components/Header/Header.vue";
import Categories from "@/components/Header/Categories.vue";
import Footer from "@/components/Footer/Footer.vue";
import Banner from "@/components/Banner/Banner.vue";
import ArticleCarousel from "@/components/ArticleCarousel/ArticleCarousel.vue";
import Feed from "@/components/Feed/Feed.vue";
import ImageCarousel from "@/components/ImageCarousel/ImageCarousel.vue";
export default {
  components: {
    Header,
    Categories,
    Footer,
    Banner,
    ArticleCarousel,
    Feed,
    ImageCarousel,
  },
};
</script>

<template>
  <Header></Header>
  <Categories></Categories>
  <Banner size="big"></Banner>
  <ArticleCarousel></ArticleCarousel>
  <Feed></Feed>
  <Banner size="big"></Banner>
  <ImageCarousel></ImageCarousel>
  <Footer></Footer>
</template>
