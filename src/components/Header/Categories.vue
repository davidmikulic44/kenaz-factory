<script setup>
  import { ref } from 'vue';
  import './styles/_categories.scss';
  import { useRouter } from 'vue-router';

  const categoryList = ['news', 'business', 'sport', 'life', 'tech', 'travel'];

  const activeCategory = ref('news');

  const router = useRouter();

  const getCategoryLink = (category) => {
    return category === 'news' ? '/' : '/category';
  };

  const handleClick = (category) => {
    activeCategory.value = category;
    console.log(activeCategory.value);
    router.push({ path: getCategoryLink(category) });
  };
</script>

<template>
  <div class="header-container-big secondary">
    <header class="header-container">
      <div class="main-navigation">
        <router-link
          v-for="(category, index) in categoryList"
          :key="index"
          class="category-nav-item"
          :class="{ 'active': activeCategory === category }"
          @click="handleClick(category)"
          :to="getCategoryLink(category)"
          :id="category.toLowerCase()"
        >
          {{ category }}
        </router-link>
      </div>
    </header>
  </div>
</template>
