<script setup>
  import { ref } from 'vue';
  import './styles/_categories.scss';

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
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'category1' }"
          @click="handleClick('category1')"
          id="category1"
        >
          news
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'category2' }"
          @click="handleClick('category2')"
          id="category2"
        >
          business
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'category3' }"
          @click="handleClick('category3')"
          id="category3"
        >
          sport
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'category4' }"
          @click="handleClick('category4')"
          id="category4"
        >
          life
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'category5' }"
          @click="handleClick('category5')"
          id="category5"
        >
          tech
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'category6' }"
          @click="handleClick('category6')"
          id="category6"
        >
          travel
        </li>
      </ul>
    </header>
  </div>
</template>