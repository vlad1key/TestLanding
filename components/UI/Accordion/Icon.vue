<script setup lang="ts">

export type AccordionIcon = {
    name?: string
    mode?: "svg" | "css"
}

const {name = "stash:plus", mode = "svg"} = defineProps<AccordionIcon>()

</script>

<template>
	<div class="flex justify-center items-center">
		<Icon :name="name" :mode="mode"></Icon>
	</div>
</template>
