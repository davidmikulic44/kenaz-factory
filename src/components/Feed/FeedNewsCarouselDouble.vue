<script setup>
    import '@splidejs/vue-splide/css';
    
    const splideOptions = {
        rewind: true,
        pagination: false,
        arrows: true,
    }
</script>


<template>
    <div class="news-carousel-container">
        <div class="feed-header">
            <h1 class="feed-title">News Carousel</h1>
            
        </div>
        
            <Splide :options="splideOptions">
                <SplideSlide>
                    <section class="feed-articles">
                        <article class="feed-single-article big-article">
                            <img src="../../assets/banner.jpg" 
                            class="feed-article-image big-article-image">
                            <div class="footer-post-header">
                                <h6 class="footer-post-info">January 19, 2024</h6>
                                <h6 class="footer-post-info">20</h6>
                            </div>
                            <h3 class="feed-article-title">For Obama, MLK's shadow looms large ahead of speech</h3>
                        </article>
                        <article class="feed-single-article big-article">
                            <img src="../../assets/planine-u-sloveniji-scaled.jpg" class="feed-article-image big-article-image">
                            <div class="footer-post-header">
                                <h6 class="footer-post-info">January 19, 2024</h6>
                                <h6 class="footer-post-info">20</h6>
                            </div>
                            <h3 class="feed-article-title">For Obama, MLK's shadow looms large ahead of speech</h3>
                        </article>
                    </section>
                </SplideSlide>
                <SplideSlide>
                    <section class="feed-articles">
                        <article class="feed-single-article big-article">
                            <img src="../../assets/banner.jpg" 
                            class="feed-article-image big-article-image">
                            <div class="footer-post-header">
                                <h6 class="footer-post-info">January 19, 2024</h6>
                                <h6 class="footer-post-info">20</h6>
                            </div>
                            <h3 class="feed-article-title">For Obama, MLK's shadow looms large ahead of speech</h3>
                        </article>
                        <article class="feed-single-article big-article">
                            <img src="../../assets/banner.jpg" class="feed-article-image big-article-image">
                            <div class="footer-post-header">
                                <h6 class="footer-post-info">January 19, 2024</h6>
                                <h6 class="footer-post-info">20</h6>
                            </div>
                            <h3 class="feed-article-title">For Obama, MLK's shadow looms large ahead of speech</h3>
                        </article>
                    </section>
                </SplideSlide>
            </Splide>
         
    </div>
</template>