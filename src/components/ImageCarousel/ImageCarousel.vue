  <script setup>
  import { ref, onMounted } from 'vue';
  import { Splide, SplideSlide, SplideTrack } from "@splidejs/vue-splide";
  import "@splidejs/vue-splide/css";
  import './styles/_imageCarousel.scss';

  let mainSplide = ref(null); 
  const main = ref();
  const thumbs = ref();

  const images = [
    {url: "/src/assets/ImageCarousel/BigImage1.jpg", id: 1},
    {url: "/src/assets/ImageCarousel/Image1.jpg", id: 2},
    {url: "/src/assets/ImageCarousel/Image2.jpg", id: 3},
    {url: "/src/assets/ImageCarousel/Image3.jpg", id: 4},
    {url: "/src/assets/ImageCarousel/Image4.jpg", id: 5},
    {url: "/src/assets/ImageCarousel/Image5.jpg", id: 6},
    {url: "/src/assets/ImageCarousel/Image6.jpg", id: 7},
  ];

  //const currentImageSrc = ref(images[currentImageIndex.value]);

  const splideOptions = {
    type: "fade",
    heightRatio: 0.5,
    pagination: false,
    arrows: true,
    cover: true,
  };

  /*const changeImageSize = () => {
    imageZoomed.value = !imageZoomed.value;
    updateBodyScroll();
  };

  const closeModal = () => {
    imageZoomed.value = false;
    updateBodyScroll();
  };

  const updateBodyScroll = () => {
    const body = document.body;
    if (imageZoomed.value) {
      body.style.overflow = 'hidden';
    } else {
      body.style.overflow = '';
    }
  };*/

  const thumbnailOptions = {
    fixedWidth: 120,
    fixedHeight: 120,
    isNavigation: true,
    gap: 10,  
    pagination: false,
    cover: true,
    arrows: false,
  };

  const selectThumbnail = (index) => {
    console.log('Thumbnail clicked, index:', index);

    if (mainSplide.value) {
      console.log('mainSplide:', mainSplide.value);
      try {
        mainSplide.value.go(index - 1);
        console.log('go method called successfully');
      } catch (error) {
        console.error('Error calling go method:', error);
      }
    }
  };
  onMounted(() => {
    mainSplide.value = main.value.splide;
    mainSplide.value.sync(thumbs.value.splide);
  });

  </script>

  <template>

     

      <div
        class="image-carousel"
        
      >
      <Splide ref="main" :options="splideOptions">
          <SplideSlide v-for="image in images" :key="image.id">
              <div class="img-container">
                <img :src="image.url" class="image-carousel-image">
              
            </div>
          </SplideSlide>
        </Splide>
      
      <div class="thumbnail-carousel">
        <Splide ref="thumbs" :options="thumbnailOptions" class="image-carousel-thumbnails">
          <SplideTrack>
            <SplideSlide v-for="image in images" :key="image.id">
              <div class="thumbnail-carousel-image" @click="selectThumbnail(image.id)">
                <img class="thumbnail-image" :src="image.url" />
              </div>
            </SplideSlide>
          </SplideTrack>
        </Splide>
      </div></div>
  </template>