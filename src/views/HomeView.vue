<template>
    
        <Header></Header>
        <Categories></Categories>
        <Banner></Banner>
        <ImageCarousel></ImageCarousel>
        <Footer></Footer>
    
</template>
<script>
    import Header from '@/components/Header/Header.vue';
    import Categories from '@/components/Header/Categories.vue';
    import Footer from '@/components/Footer/Footer.vue';
    import Banner from '@/components/Banner/Banner.vue'
    import ImageCarousel from '@/components/ImageCarousel/ImageCarousel.vue'

    export default {
        components: {
            Header,
            Categories,
            Footer,
            Banner,
            ImageCarousel,
        },
    }

</script>