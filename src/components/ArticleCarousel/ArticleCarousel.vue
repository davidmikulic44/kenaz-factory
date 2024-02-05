<script setup>
    import '@splidejs/vue-splide/css';
    import './_articleCarousel.scss';
    const splideOptions = {
        rewind: true,
        pagination: false,
        arrows: true,
        arrowPath: "M8.98536 50.0001C9.58857 50.0001 10.1672 49.7507 10.5937 49.3051L32.2873 26.6774C33.1756 25.7512 33.1756 24.2494 32.2873 23.3231L10.5937 0.695205C10.1672 0.249846 9.58857 0.000534058 8.98536 0.000534058C8.38218 0.000534058 7.80358 0.249846 7.37709 0.695205L1.64085 6.67859C0.75248 7.60481 0.75248 9.10737 1.64085 10.0336L15.9896 25.0007L1.64085 39.967C0.75248 40.8932 0.75248 42.3958 1.64085 43.322L7.37709 49.3051C7.80358 49.7507 8.38218 50.0001 8.98536 50.0001Z",
    };
</script>

<template>
    <div class="carousel">
        <Splide :options="splideOptions">
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
                    <router-link to="/article">
                        <button class="button-read-article">Read article</button>
                    </router-link>
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
            <SplideSlide>
                <div class="slide-info">
                    <div class="slide-detail">
                        <h6 class="slide-detail-text">January 19, 2024</h6>
                        <h6 class="slide-detail-text">
                            <img src="../../assets/comment ico.svg">
                            300 comments
                        </h6>
                    </div>
                    <h1 class="slide-title">Gaming centar: projekt vrijedan 60 milijuna eura dolazi u Novsku! </h1>
                    <button class="button-read-article">Read article</button>
                </div>
                <div class="img-container">
                    <img src="../../assets/nsk.jpg" class="carousel-img">
                </div>
            </SplideSlide>
        </Splide>
    </div>

</template>