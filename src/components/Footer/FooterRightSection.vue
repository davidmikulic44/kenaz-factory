<script setup>
    import './styles/_footerrightsection.scss'
    import './styles/_footer.scss'
    import FooterTagsWidget from './FooterTagsWidget.vue';
</script>

<template>
    <section class="footer-section-container">
        <div class="title-container">
            <h1 class="footer-title-dim">Tags Widget</h1>
        </div>
        <FooterTagsWidget></FooterTagsWidget>
        <h1 class="footer-posts-title">Twitter feed</h1>
        <div class="footer-tweets">
            <div class="single-tweet">
                <div class="tweet-header">
                    <img src="../../assets/tweet-icon.svg">
                    <h3 class="tweet-title">Envato @envato</h3>
                </div>
                <p class="tweet-content">Is this your typical million dollar day in the park? http://enva.to/150vxFC  Happy @TrueThemes Day! #ThemeForest pic.twitter.com/EHz7awxOXy</p>
            </div>
        </div>
    </section>
</template>
