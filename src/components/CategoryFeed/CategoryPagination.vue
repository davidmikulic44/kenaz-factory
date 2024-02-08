<script setup>
import { ref } from "vue";
const pagesList = ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10"];
const selectedPage = ref("1");

const handleClick = (page) => {
  selectedPage.value = page;
};
</script>

<template>
  <div class="page-boxes">
    <div
      class="page-box"
      v-for="(page, index) in pagesList"
      :key="index"
      @click="handleClick(page)"
      :id="page"
      :class="{ 'selected-page': selectedPage === page }"
    >
      {{ page }}
    </div>
  </div>
</template>
