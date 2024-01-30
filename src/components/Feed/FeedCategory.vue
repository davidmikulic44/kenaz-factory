<script setup>
const props = defineProps(['category']);
</script>

<template>
    <section class="feed-single-section" :class="category">
        <div class="feed-header">
            <h1 class="feed-title">{{ category }}</h1>
            <a href="#" class="feed-read-all">See all</a>
        </div>
        <section class="feed-articles">
            <article class="feed-single-article">
                <img src="../../assets/banner.jpg" class="feed-article-image">
                <div class="footer-post-header">
                    <h6 class="footer-post-info">January 19, 2024</h6>
                    <h6 class="footer-post-info">20</h6>
                </div>
                <h3 class="feed-article-title">For Obama, MLK's shadow looms large ahead of speech</h3>
            </article>
            <article class="feed-single-article">
                <img src="../../assets/banner.jpg" class="feed-article-image">
                <div class="footer-post-header">
                    <h6 class="footer-post-info">January 19, 2024</h6>
                    <h6 class="footer-post-info">20</h6>
                </div>
                <h3 class="feed-article-title">For Obama, MLK's shadow looms large ahead of speech</h3>
            </article>
            <article class="feed-single-article">
                <img src="../../assets/banner.jpg" class="feed-article-image">
                <div class="footer-post-header">
                    <h6 class="footer-post-info">January 19, 2024</h6>
                    <h6 class="footer-post-info">20</h6>
                </div>
                <h3 class="feed-article-title">For Obama, MLK's shadow looms large ahead of speech</h3>
            </article>
        </section>
        
    </section>
</template>