<script setup>
    import './styles/_feed.scss';
    import FeedCategory from './FeedCategory.vue';
    import Banner from '../Banner/Banner.vue';
    import FeednewsCarousel from './FeedNewsCarousel.vue'
    import FeedDoubleCarousel from './FeedDoubleCarousel.vue';
    import Sidebar from '../Sidebar/Sidebar.vue';
</script>

<template>
    <div class="feed-container">
        <div class="feed-column1">
            <FeedCategory category="news" numArticles="3"></FeedCategory>
            <FeedCategory category="sport" numArticles="3"></FeedCategory>
            <Banner size="mid"></Banner>
            <FeedCategory category="business" numArticles="4"></FeedCategory>
            <Banner size="mid"></Banner>
            <FeednewsCarousel></FeednewsCarousel>
            <FeedDoubleCarousel></FeedDoubleCarousel>
        </div>
        <div class="feed-column2">
            <Sidebar></Sidebar>
        </div>
    </div>
</template>