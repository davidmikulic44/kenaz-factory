<script setup>
    import './styles/_footermidsection.scss'
    import './styles/_footer.scss'
    import FooterPosts from './FooterPosts.vue'
</script>

<template>
    <section class="footer-section-container">
        <div class="title-container">
            <h1 class="footer-title-dim">Newsletter</h1>
        </div>
        <p class="footer-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus leo ante.</p>
        <form class="subscription-container" method="" action="">
            <input class="subscription-input" type="email" placeholder="Your email">
            <input class="subscription-submit" type="submit" value="Subscribe">
        </form>
        <h1 class="footer-posts-title">Random posts</h1>
        <FooterPosts></FooterPosts>
    </section>
</template>