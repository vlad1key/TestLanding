<script setup lang="ts">

export type AccordionItem = {
    id: string
    header?: string
    iconName?: string    
    iconMode?: "svg" | "css"    
    content?: string
}

const { props } = defineProps<{props: AccordionItem}>()

</script>

<template>
	<AccordionItem :value="props?.id">
		<AccordionHeader>
			<AccordionTrigger>
				<header
				class="data-[state=open]:[&>last:div>*]:rotate-180 flex justify-between items-center"
				>
					<h3 class="font-medium">
						<slot name="header-text">{{ props?.header || "Заголовок" }}</slot>
					</h3>
					<UIAccordionIcon :name="props?.iconName" :mode="props?.iconMode"></UIAccordionIcon>
				</header>
			</AccordionTrigger>
		</AccordionHeader>
		<AccordionContent><slot name="content"><p>{{ props?.content }}</p></slot></AccordionContent>
	</AccordionItem>
</template>
