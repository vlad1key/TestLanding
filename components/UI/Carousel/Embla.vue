<script setup lang="ts">
import emblaCarouselVue from "embla-carousel-vue";

const [emblaRef, emblaApi] = emblaCarouselVue({ loop: false, dragFree: true });

// onMounted(() => {
//   if (emblaApi.value) {
//     console.log(emblaApi.value.slideNodes()) // Access API
//   }
// })
// <img class="flex relative rounded-2xl" :src="slide.imgSrc" alt="Slide image" />

</script>

<template>
	<div class="embla overflow-scroll" ref="emblaRef">
		<slot></slot>
	</div>
</template>
