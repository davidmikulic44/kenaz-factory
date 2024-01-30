<script setup>
  import { ref, onMounted } from 'vue';
  import './styles/_categories.scss';
  import { useRouter } from 'vue-router';

  const categoryList = ['news', 'business', 'sport', 'life', 'tech', 'travel'];

  const activeCategory = ref(localStorage.getItem('activeCategory') || 'news');

  const router = useRouter();

  const handleClick = (category) => {
    if (category === 'news') {
      activeCategory.value = 'news';
      localStorage.setItem('activeCategory', 'news');
      router.push('/');
    } else {
      activeCategory.value = category;
      localStorage.setItem('activeCategory', category);
      router.push({ path: getCategoryLink(category) });
    }
  };

  onMounted(() => {
    if (!activeCategory.value) {
      activeCategory.value = 'news';
    }
  });

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
          to="/category"
          :id="category.toLowerCase()"
        >
          {{ category }}
        </router-link>
      </div>
    </header>
  </div>
</template>
