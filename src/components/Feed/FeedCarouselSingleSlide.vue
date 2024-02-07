<script setup>
    import FeedCarouselSingleArticle from './FeedCarouselSingleArticle.vue';
</script>

<template>
    <SplideSlide>
        <section class="feed-articles">
            <FeedCarouselSingleArticle size="big-article"></FeedCarouselSingleArticle>
            <FeedCarouselSingleArticle size="big-article"></FeedCarouselSingleArticle>
        </section>
    </SplideSlide>
</template>