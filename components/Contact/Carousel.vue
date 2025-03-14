<script setup lang="ts">
import emblaCarouselVue from "embla-carousel-vue";

const [emblaRef, emblaApi] = emblaCarouselVue({ loop: false , dragFree: true});

export type Dimension = {
	id: number;
	title: string;
    xyz: [number, number, number]
	image?: string;
};

const dimensionsList = ref<Dimension[]>([
	{ id: 1, title: "Габарит 1", xyz: [100, 100, 100]},
	{ id: 2, title: "Габарит 2", xyz: [150, 150, 150] },
	{ id: 3, title: "Габарит 3", xyz: [200, 200, 200] },
	{ id: 4, title: "Габарит 4", xyz: [250, 250, 250] },
	{ id: 5, title: "Габарит 5", xyz: [300, 300, 300] },
	{ id: 6, title: "Габарит 6", xyz: [350, 350, 350] },
	{ id: 7, title: "Габарит 7", xyz: [400, 400, 400] },
	{ id: 8, title: "Габарит 8", xyz: [450, 450, 450] },
]);

const selectedIndex = ref<number | null>(null);

const emit = defineEmits<{
    select: [dimension: Dimension]
}>()

emit("select", dimensionsList.value[0])

</script>

<template>
	<div
	 class="embla flex h-15 relative flew-wrap justify-between items-center max-w-full overflow-scroll"
	 ref="emblaRef"
	>
		<div class="embla__container flex h-full w-full absolute gap-3">
			<div
			 v-for="(dimension, index) in dimensionsList"
			 :key="dimension.id"
			 class="embla__slide flex-[0_0_fit-content] rounded-xl flex select-none bg-gray-50"
             @click="$emit('select', dimension)"
             >
				<input :checked="index === 0" type="radio" name="dimension" :id="`dimension-${dimension.id}`" :value="dimension.id" class="hidden peer">
				<label :for="`dimension-${dimension.id}`" class="flex p-3 gap-2 justify-between items-center border border-white peer-checked:border-black box-border rounded-xl">
					<div class="flex justify-center items-center">
						<img
						 v-if="dimension?.image"
						 :src="dimension.image"
						 alt="img"
						/>
                        <Icon
						 v-else
						 name="hugeicons:package-dimensions-02"
						 mode="svg"
						 class="w-9 h-9 bg-blue-400 rounded-full"
						/>
					</div>
					
					<div class="flex flex-col justify-center">
						<h3 class="font-medium">{{ dimension.title }}</h3>
						<p class="text-sm opacity-60 font-medium">{{ dimension.xyz.join("&nbsp;x&nbsp;") }}</p>
					</div>
				</label>
			</div>
		</div>
	</div>
</template>
