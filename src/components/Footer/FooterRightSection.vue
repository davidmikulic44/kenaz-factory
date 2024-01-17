<script setup>
    import './styles/_footerrightsection.scss'
    import './styles/_footer.scss'
    import FooterTagsWidget from './FooterTagsWidget.vue';
    import FooterTwitterFeed from './FooterTwitterFeed.vue'
</script>

<template>
    <section class="footer-section-container">
        <div class="title-container">
            <h1 class="footer-title-dim">Tags Widget</h1>
        </div>
        <FooterTagsWidget></FooterTagsWidget>
        
    </section>
</template>
