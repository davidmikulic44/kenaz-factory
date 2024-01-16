<template>
    <Header></Header>
    <Categories></Categories>
    <Footer></Footer>
</template>
<script>
    import Header from '@/components/Header/Header.vue';
    import Categories from '@/components/Header/Categories.vue';
    import Footer from '@/components/Footer/Footer.vue';
    export default {
        components: {
            Header,
            Categories,
            Footer
        },
    }
</script>