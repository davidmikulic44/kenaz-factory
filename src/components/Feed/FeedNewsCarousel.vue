<script setup>
    import '@splidejs/vue-splide/css';
    
    const splideOptions = {
        rewind: true,
        pagination: false,
        arrows: true,
        classes: {
            arrow: 'news-double',
        },
        arrowPath: "M2.99453 19.0001C3.22074 19.0001 3.4377 18.9052 3.59763 18.736L11.7328 10.1374C12.0659 9.78539 12.0659 9.21486 11.7328 8.86289L3.59763 0.26423C3.4377 0.0949841 3.22074 0.000120044 2.99453 0.000120044C2.76832 0.000120044 2.55136 0.0949841 2.39142 0.26423L0.24032 2.5378C-0.0928 2.88978 -0.0928 3.46081 0.24032 3.81279L5.62114 9.50025L0.24032 15.1875C-0.0928 15.5394 -0.0928 16.1105 0.24032 16.4624L2.39142 18.736C2.55136 18.9052 2.76832 19.0001 2.99453 19.0001Z",
    };
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