<script setup>
    import './styles/_footer.scss'
    import FooterSocial from './FooterSocial.vue';
    import FooterNewsletter from './FooterNewsletter.vue';
    import FooterTagsWidget from './FooterTagsWidget.vue';
    import FooterSiteInfo from './FooterSiteInfo.vue';
    import FooterFeaturedPosts from './FooterFeaturedPosts.vue';
    import FooterRandomPosts from './FooterRandomPosts.vue';
    import FooterTwitterFeed from './FooterTwitterFeed.vue';
</script>

<template>
    <footer class="footer-container-big">
        <div class="footer-primary">
            <div class="footer-row1">
                <FooterSocial></FooterSocial>
                <FooterNewsletter></FooterNewsletter>
                <FooterTagsWidget></FooterTagsWidget>
            </div>
            <div class="footer-row2">
                <FooterFeaturedPosts></FooterFeaturedPosts>
                <FooterRandomPosts></FooterRandomPosts>
                <FooterTwitterFeed></FooterTwitterFeed>
            </div>
        </div>
        <img src="../../assets/BigLine.svg">
        <div class="footer-secondary">
            <FooterSiteInfo></FooterSiteInfo>
        </div>
    </footer>
    
</template>