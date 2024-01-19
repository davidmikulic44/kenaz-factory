<script setup>
    import './styles/_feed.scss';
    import FeedNews from './FeedNews.vue';
    import FeedSport from './FeedSport.vue';
</script>

<template>
    <div class="feed-container">
        <div class="feed-column1">
            <FeedNews></FeedNews>
            <FeedSport></FeedSport>
        </div>
        <div class="feed-column2">

        </div>
    </div>
</template>