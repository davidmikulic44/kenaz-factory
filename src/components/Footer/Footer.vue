<script setup>
    import './styles/_footer.scss'
    import FooterLeftSection from './FooterLeftSection.vue';
    import FooterMidSection from './FooterMidSection.vue';
    import FooterRightSection from './FooterRightSection.vue';
    import FooterSiteInfo from './FooterSiteInfo.vue';
    import FooterFeaturedPosts from './FooterFeaturedPosts.vue';
    import FooterRandomPosts from './FooterRandomPosts.vue';
    import FooterTwitterFeed from './FooterTwitterFeed.vue';
</script>

<template>
    <footer class="footer-container-big">
        <div class="footer-primary">
            <div class="footer-row1">
                <FooterLeftSection></FooterLeftSection>
                <FooterMidSection></FooterMidSection>
                <FooterRightSection></FooterRightSection>
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