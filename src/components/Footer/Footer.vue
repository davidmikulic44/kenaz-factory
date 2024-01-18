<script setup>
    import './styles/_footer.scss'
    import SocialLinks from './SocialLinks.vue';
    import Newsletter from './Newsletter.vue';
    import TagsWidget from './TagsWidget.vue';
    import SiteInfo from './SiteInfo.vue';
    import FeaturedPosts from './FeaturedPosts.vue';
    import RandomPosts from './RandomPosts.vue';
    import TwitterFeed from './TwitterFeed.vue';
</script>

<template>
    <footer class="footer-container-big">
        <div class="footer-primary">
            <div class="footer-row1">
                <SocialLinks></SocialLinks>
                <Newsletter></Newsletter>
                <TagsWidget></TagsWidget>
            </div>
            <div class="footer-row2">
                <FeaturedPosts></FeaturedPosts>
                <RandomPosts></RandomPosts>
                <TwitterFeed></TwitterFeed>
            </div>
        </div>
        <img src="../../assets/BigLine.svg">
        <div class="footer-secondary">
            <SiteInfo></SiteInfo>
        </div>
    </footer>
    
</template>