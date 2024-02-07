<script setup>
import { ref, onMounted } from 'vue';
import { Splide, SplideSlide, SplideTrack } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";
import './styles/_imageCarousel.scss';

let imageZoomed = ref(false);
let currentImageIndex = ref(0);
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

const currentImageSrc = ref(images[0]);

const splideOptions = {
	type: "fade",
	heightRatio: 0.5,
	pagination: false,
	arrows: true,
	cover: true,
	arrowPath: "M8.98536 50.0001C9.58857 50.0001 10.1672 49.7507 10.5937 49.3051L32.2873 26.6774C33.1756 25.7512 33.1756 24.2494 32.2873 23.3231L10.5937 0.695205C10.1672 0.249846 9.58857 0.000534058 8.98536 0.000534058C8.38218 0.000534058 7.80358 0.249846 7.37709 0.695205L1.64085 6.67859C0.75248 7.60481 0.75248 9.10737 1.64085 10.0336L15.9896 25.0007L1.64085 39.967C0.75248 40.8932 0.75248 42.3958 1.64085 43.322L7.37709 49.3051C7.80358 49.7507 8.38218 50.0001 8.98536 50.0001Z",
};

const changeImageSize = () => {
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
};

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
if (mainSplide.value) {
	console.log('mainSplide:', mainSplide.value);
	try {
	mainSplide.value.go(index - 1);
	} catch (error) {
	console.error('Error calling go method:', error);
	}
}
};
onMounted(() => {
	mainSplide.value = main.value.splide;
	mainSplide.value.sync(thumbs.value.splide);

	mainSplide.value.on('moved', (newIndex) => {
		currentImageSrc.value = images[newIndex];
	});
});

</script>

<template>
	<div v-if="imageZoomed" class="modal" @click="closeModal">
		<img :src="currentImageSrc.url" class="modal-content"/>
	</div>

	<div
	class="image-carousel"
	:key="imageZoomed.value"
	>
	<Splide ref="main" :options="splideOptions">
		<SplideSlide v-for="image in images" :key="image.id">
			<div class="img-container" :style="{backgroundImage: image.url}">
				<img :src="image.url" class="image-carousel-image carousel-img">
			</div>
				<div class="image-carousel-search-icon" @click="changeImageSize">
				<img v-if="!imageZoomed" src="../../assets/SearchIcon.svg" />
			</div>
		
		</SplideSlide>
	</Splide>
	
		<div class="thumbnail-carousel">
			<Splide 
			ref="thumbs" 
			:options="thumbnailOptions" 
			class="image-carousel-thumbnails">
				<SplideTrack>
					<SplideSlide v-for="image in images" :key="image.id">
						<div class="thumbnail-carousel-image" 
						@click="selectThumbnail(image.id)">
							<img class="thumbnail-image" :src="image.url" />
						</div>
					</SplideSlide>
				</SplideTrack>
			</Splide>
		</div>
	</div>
</template>