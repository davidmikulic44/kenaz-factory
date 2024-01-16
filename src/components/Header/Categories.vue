<script setup>
  import { ref } from 'vue';
  import './styles/_categories.scss';

  const activeCategory = ref('news');

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
          :class="{ 'active': activeCategory === 'news' }"
          @click="handleClick('news')"
          id="category1"
        >
          news
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'business' }"
          @click="handleClick('business')"
          id="category2"
        >
          business
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'sport' }"
          @click="handleClick('sport')"
          id="category3"
        >
          sport
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'life' }"
          @click="handleClick('life')"
          id="category4"
        >
          life
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'tech' }"
          @click="handleClick('tech')"
          id="category5"
        >
          tech
        </li>
        <li
          class="category-nav-item"
          :class="{ 'active': activeCategory === 'travel' }"
          @click="handleClick('travel')"
          id="category6"
        >
          travel
        </li>
      </ul>
    </header>
  </div>
</template>