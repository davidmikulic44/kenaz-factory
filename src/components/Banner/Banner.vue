<script setup>
import "./_banner.scss";
const props = defineProps(["size"]);
</script>

<template>
  <img
    src="../../assets/banner.jpg"
    class="banner-image"
    :class="size"
    alt=""
  />
</template>
