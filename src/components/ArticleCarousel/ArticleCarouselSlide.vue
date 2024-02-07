<script setup>
const props = defineProps(['date', 'comments', 'title', 'image']);
</script>

<template>
    <SplideSlide>
        <div class="slide-info">
            <div class="slide-detail">
                <h6 class="slide-detail-text">{{ date }}</h6>
                <h6 class="slide-detail-text">
                    <img src="../../assets/comment ico.svg">
                    {{ comments }}
                </h6>
            </div>
            <h1 class="slide-title">{{ title }}</h1>
            <router-link to="/article">
                <button class="button-read-article">Read article</button>
            </router-link>
        </div>
        <div class="img-container">
            <img :src="image" class="carousel-img">
        </div>
    </SplideSlide>
</template>