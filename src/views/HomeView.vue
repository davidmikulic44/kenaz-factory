<template>
        <Header></Header>
        <Categories></Categories>
        <BannerBig></BannerBig>
        <ImageCarousel></ImageCarousel>
        <Feed></Feed>
        <BannerBig></BannerBig>
        <Footer></Footer>
    
</template>
<script>
    import Header from '@/components/Header/Header.vue';
    import Categories from '@/components/Header/Categories.vue';
    import Footer from '@/components/Footer/Footer.vue';
    import BannerBig from '@/components/Banner/BannerBig.vue'
    import ImageCarousel from '@/components/ImageCarousel/ImageCarousel.vue'
    import Feed from '@/components/Feed/Feed.vue';
    export default {
        components: {
            Header,
            Categories,
            Footer,
            BannerBig,
            ImageCarousel,
            Feed,
        },
    }

</script>