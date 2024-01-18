<script setup>
    
    let selectedTags = reactive([]);

    const toggleTag = (tagId) => {
        const index = selectedTags.indexOf(tagId);
        if (index === -1) {
            selectedTags.push(tagId);
        } else {
            selectedTags.splice(index, 1);
        }
    };
</script>

<template>
    <section class="footer-section-container">
        <div class="title-container">
                <h1 class="footer-title-dim">Tags Widget</h1>
        </div>
        <ul class="footer-tags">
            <li 
                v-for="(tag) in ['assueverit', 'utroquoe', 'probo', 'assuev', 'dolor', 'adipiscing', 'elit', 'neque', 'vestibulum', 'mattis', 'lorem', 'consectetur', 'fusce']"
                :key="tag"
                :class="{ 'footer-single-tag': true, 'active-tag': selectedTags.includes(tag) }"
                @click="toggleTag(tag)"
            >
                {{ tag }}
            </li>
        </ul>
    </section>
</template>
