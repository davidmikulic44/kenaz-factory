<script setup>
    import './styles/_footer.scss'
    import FooterLeftSection from './FooterLeftSection.vue';
    import FooterMidSection from './FooterMidSection.vue';
    import FooterRightSection from './FooterRightSection.vue';
</script>

<template>
    <div class="footer-container-big">
        <footer class="footer-container">
            <FooterLeftSection></FooterLeftSection>
            <FooterMidSection></FooterMidSection>
            <FooterRightSection></FooterRightSection>
        </footer>
    </div>

</template>