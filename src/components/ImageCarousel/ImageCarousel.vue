<script setup>
    import './_imageCarousel.scss';
    import '@splidejs/vue-splide/css';

   

</script>

<template>
    <div class="carousel">
        <Splide :options="{ rewind: true }" aria-label="My Favorite Images">
            <SplideSlide>
                <div class="slide-info">
                    <div class="slide-detail">
                        <h6 class="slide-detail-text">January 18, 2024</h6>
                        <h6 class="slide-detail-text">
                            <img src="../../assets/comment ico.svg">
                            22 comments
                        </h6>
                    </div>
                    <h1 class="slide-title">'Margot' breathlessly reimagines Anne Frank's sister</h1>
                    <button class="button-read-article">Read article</button>
                </div>
                <div class="img-container">
                    <img src="../../assets/planine-u-sloveniji-scaled.jpg" class="carousel-img">
                </div>
            </SplideSlide>
            <SplideSlide>
                <div class="slide-info">
                    <div class="slide-detail">
                        <h6 class="slide-detail-text">January 18, 2024</h6>
                        <h6 class="slide-detail-text">
                            <img src="../../assets/comment ico.svg">
                            30 comments
                        </h6>
                    </div>
                    <h1 class="slide-title">Speech by the President: European Parliament Plenary</h1>
                    <button class="button-read-article">Read article</button>
                </div>
                <div class="img-container">
                    <img src="../../assets/banner.jpg" class="carousel-img">
                </div>
            </SplideSlide>
        </Splide>
    </div>

</template>