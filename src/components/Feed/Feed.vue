<script setup>
    import './styles/_feed.scss';
    import FeedNews from './FeedNews.vue';
    import FeedSport from './FeedSport.vue';
    import FeedRatedPosts from './FeedRatedPosts.vue';
    import BannerMid from '../Banner/BannerMid.vue';
    import FeedBusiness from './FeedBusiness.vue';
    import FeednewsCarouselDouble from './FeedNewsCarouselDouble.vue'
</script>

<template>
    <div class="feed-container">
        <div class="feed-column1">
            <FeedNews></FeedNews>
            <FeedSport></FeedSport>
            <BannerMid></BannerMid>
            <FeedBusiness></FeedBusiness>
            <BannerMid></BannerMid>
            <FeednewsCarouselDouble></FeednewsCarouselDouble>
        </div>
        <div class="feed-column2">
            <FeedRatedPosts></FeedRatedPosts>
        </div>
    </div>
</template>