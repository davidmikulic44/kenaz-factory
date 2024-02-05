<script setup>
    import Sidebar from '../Sidebar/Sidebar.vue';
    import Banner from '../Banner/Banner.vue';
    import CategoryArticles from './CategoryArticles.vue';
    
</script>

<template>
    <div class="feed-container">
        <div class="feed-column1">
            <CategoryArticles></CategoryArticles>
            <Banner size="mid"></Banner>
        </div>
        <div class="feed-column2">
            <Sidebar></Sidebar>
        </div>
    </div>
</template>