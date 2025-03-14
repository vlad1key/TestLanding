<!-- <script setup lang="ts">
import type { AccordionItem } from '../UI/Accordion/Item.vue';


const items: AccordionItem[] = [
	{ id: "item-1", header: "Тест заголовка", content: "Тест описания" },
	{ id: "item-2", header: "Тест заголовка 2", content: "Тест описания 2" },
	{ id: "item-3", header: "Тест заголовка 3", content: "Тест описания 3" },
	{ id: "item-4", header: "Тест заголовка 4", content: "Тест описания 4" },

] 

</script>

<template>
	<TheContainer>
		<UIAccordion>
			<UIAccordionItem 
			v-for="item of items"
			:key="item.id"
			:props="item"
			:id="item.id"
			:header="item.header"
			:content="item.content"
			> 

			</UIAccordionItem>
		</UIAccordion>
	</TheContainer>
</template> -->

<!-- 
<span>Вопрос 1</span>
<Icon 
 mode="svg" 
 name="stash:plus" 
 class="transition-transform duration-300" 
/>
 -->

<script setup lang="ts">
const accordionItems = [
	{
		value: "item-1",
		title: "Вопрос 1",
		content: "Ответ на вопрос",
	},
	{
		value: "item-2",
		title: "Вопрос 2",
		content: "Ответ на вопрос",
	},
	{
		value: "item-3",
		title: "Вопрос 3",
		content: "Ответ на вопрос",
	},
	{
		value: "item-4",
		title: "Вопрос 4",
		content: "Ответ на вопрос",
	},
	{
		value: "item-5",
		title: "Вопрос 5",
		content: "Ответ на вопрос",
	},
];
</script>

<template>
	<section id="faq">
		<TheContainer
			class="gap-5 sm:gap-[15%] w-full flex-col sm:flex-row justify-between bg-white"
		>
			<h2 class="text-4xl font-semibold">FAQ</h2>

			<AccordionRoot
				class="flex flex-col flex-grow gap-2 transition-transform"
				type="multiple"
				:collapsible="true"
				:unmount-on-hide="false"
			>
				<template v-for="item in accordionItems" :key="item.value">
					<AccordionItem
						class="rounded-2xl bg-gray-50 mt-px overflow-hidden first:mt-0 focus-within:relative focus-within:z-10 focus-within:shadow-[0_0_0_1px]"
						:value="item.value"
					>
						<AccordionHeader class="flex">
							<AccordionTrigger
								class="data-[state=open]:[&_svg]:rotate-[315deg] flex flex-1 items-center justify-between px-5 py-3 text-md font-medium leading-none shadow-[0_1px_0] outline-none"
							>
								<span>{{ item.title }}</span>
								<div class="bg-white rounded-md p-2">
									<Icon
									mode="svg"
									name="stash:plus"
									class="transition-transform"
									/>
								</div>
							</AccordionTrigger>
						</AccordionHeader>
						<AccordionContent
							class="overflow-hidden text-sm data-[state=open]:animate-(--animate-slide-down) data-[state=closed]:animate-(--animate-slide-up)"
						>
							<div class="px-5 py-4">
								{{ item.content }}
							</div>
						</AccordionContent>
					</AccordionItem>
				</template>
			</AccordionRoot>
		</TheContainer>
	</section>
</template>

<style scoped>


</style>
