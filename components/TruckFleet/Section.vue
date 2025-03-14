<script setup lang="ts">

type Slide = {
	title: string
	imgSrc: string
}

const slides: Slide[] = [
	{title: "Слайд 1", imgSrc: "/truckfleet-1.jpeg"},
	{title: "Слайд 2", imgSrc: "/truckfleet-1.jpeg"},
	{title: "Слайд 3", imgSrc: "/truckfleet-1.jpeg"},
	{title: "Слайд 4", imgSrc: "/truckfleet-1.jpeg"},
	{title: "Слайд 5", imgSrc: "/truckfleet-1.jpeg"},
]

</script>

<template>
	<section id="trucks" class="flex">
		<TheContainer class="flex-col w-full bg-white">
			<h2 class="text-4xl font-semibold">Наш автопарк</h2>
			<UICarouselEmbla>
				<UICarouselContainer class="flex gap-2">
					<UICarouselSlide 
					v-for="slide in slides" :key="slide.title"
					class="flex flex-shrink-0 flex-grow-0 sm:basis-[23vw] basis-[90%] aspect-[6/5] select-none"
					>
						<div class="flex justify-center items-end relative h-full w-full">
							<img :src="slide.imgSrc" alt="slide image" class="absolute w-full h-full rounded-2xl -z-10">
							<div class="flex items-center mb-3 mx-3 p-2 w-full bg-white rounded-2xl">
								<h3 class="font-medium text-sm"> {{slide.title}} </h3>
							</div>    
						</div>
					</UICarouselSlide>
				</UICarouselContainer>
			</UICarouselEmbla>
		</TheContainer>
	</section>
</template>
