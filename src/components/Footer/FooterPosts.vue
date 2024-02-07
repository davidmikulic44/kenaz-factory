<script setup>
    import FooterPostSingle from './FooterPostSingle.vue';

    const props = defineProps(['title']);

</script>

<template>
    <section class="footer-posts">
        <h1 class="footer-posts-title">{{ title }}</h1>
            <FooterPostSingle date="January 16, 2024" readTime="7" title="Konferencija “Man of Steel” u Novskoj"></FooterPostSingle>
            <FooterPostSingle date="January 16, 2024" readTime="7" title="Konferencija “Man of Steel” u Novskoj"></FooterPostSingle>
            <FooterPostSingle date="January 16, 2024" readTime="7" title="Konferencija “Man of Steel” u Novskoj"></FooterPostSingle>
        </section>
</template>