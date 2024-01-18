<script setup>
  import { ref } from 'vue';
  import './styles/_categories.scss';

  const categoryList = ['news', 'business', 
                        'sport', 'life',
                        'tech', 'travel',]

  const activeCategory = ref('category1');

  const handleClick = (category) => {
    activeCategory.value = category;
  };
</script>

<template>
  <div class="header-container-big secondary">
    <header class="header-container">
      <ul class="main-navigation">
        <li
          v-for="(category, index) in categoryList"
          :key="index"
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'category' + (index + 1) }"
          @click="handleClick('category' + (index + 1))"
          :id="'category' + (index + 1)"
        >
          {{ category }}
        </li>
      </ul>
    </header>
  </div>
</template>
