<template>
  <div>
    <div v-if="isEnlargedImage" class="modal" @click="closeModal">
      <div class="modal-content">
        <img :src="currentImageSrc" />
      </div>
    </div>

    <div
      :class="{
        'home-gallery': !isEnlargedImage,
        'home-gallery-enlarged': isEnlargedImage,
      }"
      :key="isEnlargedImage.value"
    >
      <Splide
        class="splide-home-gallery"
        ref="main"
        :options="mainOptionsData"
        aria-label="Home Gallery Images"
        @moved="updateCurrentImage"
      >
        <SplideSlide v-for="(image, index) in images" :key="index">
          <div class="home-gallery__image">
            <img :src="image" />
            <div class="home-gallery__search-icon" @click="changeImageSize">
              <img v-if="!isEnlargedImage" src="../../assets/SearchIcon.svg" />
            </div>
          </div>
        </SplideSlide>
      </Splide>
    </div>
  </div>
</template>

<script setup>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";
import './styles/_imageCarousel.scss';
import { ref, watch } from 'vue';

let isEnlargedImage = ref(false);
let currentImageIndex = ref(0);

const images = [
  "../../assets/ImageCarousel/BigImage1.jpg",
  "../../assets/ImageCarousel/Image2.jpg",
  // Add more images as needed
];

const currentImageSrc = ref(images[currentImageIndex.value]);

const mainOptionsData = {
  type: "fade",
  heightRatio: 0.5,
  pagination: false,
  arrows: true,
  cover: true,
};

const changeImageSize = () => {
  isEnlargedImage.value = !isEnlargedImage.value;
  updateBodyScroll();
};

const closeModal = () => {
  isEnlargedImage.value = false;
  updateBodyScroll();
};

const updateBodyScroll = () => {
  const body = document.body;
  if (isEnlargedImage.value) {
    body.style.overflow = 'hidden';
  } else {
    body.style.overflow = '';
  }
};

const updateCurrentImage = (splide) => {
  currentImageIndex.value = splide.index;
  currentImageSrc.value = images[currentImageIndex.value];
};

// Watch for changes in currentImageIndex
watch(currentImageIndex, (newIndex) => {
  currentImageSrc.value = images[newIndex];
});

</script>
