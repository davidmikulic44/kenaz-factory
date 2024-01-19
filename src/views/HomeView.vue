<template>
    
        <Header></Header>
        <Categories></Categories>
        <Banner></Banner>
        <ImageCarousel></ImageCarousel>
        <Feed></Feed>
        <Footer></Footer>
    
</template>
<script>
    import Header from '@/components/Header/Header.vue';
    import Categories from '@/components/Header/Categories.vue';
    import Footer from '@/components/Footer/Footer.vue';
    import Banner from '@/components/Banner/Banner.vue'
    import ImageCarousel from '@/components/ImageCarousel/ImageCarousel.vue'
    import Feed from '@/components/Feed/Feed.vue';
    export default {
        components: {
            Header,
            Categories,
            Footer,
            Banner,
            ImageCarousel,
            Feed,
        },
    }

</script>