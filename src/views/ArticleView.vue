<script setup>
    import Header from '@/components/Header/Header.vue';
    import Footer from '@/components/Footer/Footer.vue';
    import Categories from '@/components/Header/Categories.vue';
    import ArticleFeed from '@/components/ArticleFeed/ArticleFeed.vue';
    import Banner from '@/components/Banner/Banner.vue';
</script>

<template>
    <Header></Header>
    <Categories></Categories>
    <Banner size="big"></Banner>
    <ArticleFeed></ArticleFeed>
    <Footer></Footer>
</template>