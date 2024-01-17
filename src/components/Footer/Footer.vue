<script setup>
    import './styles/_footer.scss'
    import FooterLeftSection from './FooterLeftSection.vue';
    import FooterMidSection from './FooterMidSection.vue';
    import FooterRightSection from './FooterRightSection.vue';
    import FooterSiteInfo from './FooterSiteInfo.vue';
</script>

<template>
    <footer class="footer-container-big">
        <div class="footer-primary">
            <FooterLeftSection></FooterLeftSection>
            <FooterMidSection></FooterMidSection>
            <FooterRightSection></FooterRightSection>
        </div>
        <img src="../../assets/BigLine.svg">
        <div class="footer-secondary">
            <FooterSiteInfo></FooterSiteInfo>
        </div>
    </footer>
    
</template>