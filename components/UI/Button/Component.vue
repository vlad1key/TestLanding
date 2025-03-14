
<script setup lang="ts">
const {title = "Текст кнопки"} = defineProps<{
	title: string
}>()
</script>

<template>
	
	<button class="flex max-w-44 items-center rounded-full bg-black">
		<IconsArrow class="h-full [&_.circle-fill]:text-white" />
		<div class="flex mx-auto">
			<p class="flex items-center text-white text-sm text-opacity-90 text-nowrap mr-2">{{ title }}</p>
		</div>
	</button>
	
</template>

