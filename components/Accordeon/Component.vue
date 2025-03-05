<script setup lang="ts">
type AccordionItem = {
	value: string;
	title: string;
	content: string;
};

const props = defineProps<{
	accordionItems: AccordionItem[];
}>();
</script>

<template>
	<div>
		<AccordionRoot>
			<template v-for="item in accordionItems" :key="item.value">
				<AccordionItem :value="item.value">
					<AccordionHeader>
						<AccordionTrigger />
					</AccordionHeader>
					<AccordionContent />
				</AccordionItem>
			</template>
		</AccordionRoot>
	</div>
</template>

<style></style>
