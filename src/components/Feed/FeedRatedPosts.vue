<script setup>
    import { ref } from 'vue';
    const categoryList = ['popular', 'top rated', 'comments']

    const activeCategory = ref('popular');

    const handleClick = (category) => {
        activeCategory.value = category;
        
    }
</script>

<template>
    <aside class="rated-posts-container">
        <div class="rated-posts-header">
            <h6
            v-for="(category, index) in categoryList"
            :key="index"
            :class="{'active-rated' : activeCategory === (category)}"
            @click="handleClick(category)"
            :id="(category)"
            class="rated-posts-header-title">{{ category }}</h6>
        </div>
        <div class="posts-container">
            <div class="rated-post-single">
                <div class="rated-post-single-info">
                    <div class="rated-post-header">
                        <h6 class="rated-post-info comments">
                            <img class="rated-post-comments-icon" src="../../assets/comment ico.svg">
                            5</h6>
                        <h6 class="rated-post-info date">January 22, 2024</h6>
                    </div>
                    <h3 class="rated-post-title">Palestinians call off peace talks after clash</h3>
                </div>
                <img src="../../assets/manofsteel.jpeg" class="footer-post-image" alt="">
            </div>
            <div class="rated-post-single">
                <div class="rated-post-single-info">
                    <div class="rated-post-header">
                        <h6 class="rated-post-info comments">
                            <img class="rated-post-comments-icon" src="../../assets/comment ico.svg">
                            5</h6>
                        <h6 class="rated-post-info date">January 22, 2024</h6>
                    </div>
                    <h3 class="rated-post-title">Palestinians call off peace talks after clash</h3>
                </div>
                <img src="../../assets/manofsteel.jpeg" class="footer-post-image" alt="">
            </div>
            <div class="rated-post-single">
                <div class="rated-post-single-info">
                    <div class="rated-post-header">
                        <h6 class="rated-post-info comments">
                            <img class="rated-post-comments-icon" src="../../assets/comment ico.svg">
                            5</h6>
                        <h6 class="rated-post-info date">January 22, 2024</h6>
                    </div>
                    <h3 class="rated-post-title">Palestinians call off peace talks after clash</h3>
                </div>
                <img src="../../assets/manofsteel.jpeg" class="footer-post-image" alt="">
            </div>
            <div class="rated-post-single">
                <div class="rated-post-single-info">
                    <div class="rated-post-header">
                        <h6 class="rated-post-info comments">
                            <img class="rated-post-comments-icon" src="../../assets/comment ico.svg">
                            5</h6>
                        <h6 class="rated-post-info date">January 22, 2024</h6>
                    </div>
                    <h3 class="rated-post-title">Palestinians call off peace talks after clash</h3>
                </div>
                <img src="../../assets/manofsteel.jpeg" class="footer-post-image" alt="">
            </div>
            <div class="rated-post-single">
                <div class="rated-post-single-info">
                    <div class="rated-post-header">
                        <h6 class="rated-post-info comments">
                            <img class="rated-post-comments-icon" src="../../assets/comment ico.svg">
                            5</h6>
                        <h6 class="rated-post-info date">January 22, 2024</h6>
                    </div>
                    <h3 class="rated-post-title">Palestinians call off peace talks after clash</h3>
                </div>
                <img src="../../assets/manofsteel.jpeg" class="footer-post-image" alt="">
            </div>  
            
        </div>
    </aside>
</template>