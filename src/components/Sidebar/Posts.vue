<script setup>
    import PostSingle from './PostSingle.vue';
    import { ref } from 'vue';
    const categoryList = ['popular', 'top rated', 'comments'];

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
            <PostSingle></PostSingle>
            <PostSingle></PostSingle>
            <PostSingle></PostSingle>
            <PostSingle></PostSingle>
            <PostSingle></PostSingle>
        </div>
    </aside>
</template>