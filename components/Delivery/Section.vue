<script setup lang="ts">
type Label = {
    id: number
    title: string
    hoverColor: string
}

const labels: Label[] = [
  { id: 1, title: "Дачный переезд", hoverColor: "hover:bg-red-500" },
  { id: 2, title: "Переезд", hoverColor: "hover:bg-blue-500" },
  { id: 3, title: "Строительные материалы", hoverColor: "hover:bg-green-500" },
  { id: 4, title: "Двери", hoverColor: "hover:bg-yellow-500" },
  { id: 5, title: "Мебель", hoverColor: "hover:bg-purple-500" },
  { id: 6, title: "Техника", hoverColor: "hover:bg-pink-500" },
  { id: 7, title: "Кровати", hoverColor: "hover:bg-red-500" },
  { id: 8, title: "Вещи", hoverColor: "hover:bg-blue-500" },
  { id: 9, title: "Дачный переезд", hoverColor: "hover:bg-green-500" },
  { id: 10, title: "Переезд", hoverColor: "hover:bg-yellow-500" },
  { id: 11, title: "Строительные материалы", hoverColor: "hover:bg-purple-500" },
  { id: 12, title: "Двери", hoverColor: "hover:bg-pink-500" },
  { id: 13, title: "Мебель", hoverColor: "hover:bg-red-500" },
  { id: 14, title: "Техника", hoverColor: "hover:bg-blue-500" },
  { id: 15, title: "Кровати", hoverColor: "hover:bg-green-500" },
  { id: 16, title: "Вещи", hoverColor: "hover:bg-yellow-500" },
]


</script>

<template>
	<section id="delivery">
		<TheContainer class="flex-col bg-white">
			<h2 class="text-4xl font-semibold">Разная доставка для разных задач</h2>
			<UILabelContainer class="gap-3">
				<UILabelItem
				v-for="label in labels"
				:key="label.id"
				class="font-medium transition-color duration-200 bg-gray-100 hover:text-gray-50 cursor-default"
				:class="label.hoverColor"
				>
					{{ label.title }}
				</UILabelItem>
			</UILabelContainer>
		</TheContainer>
	</section>
</template>

<style scoped>

</style>

<!-- <script setup lang="ts">
type Label = {
	id: number,
	title: string
}

const labels: Label[] = [
	{id: 1, title: "Дачный переезд"},
	{id: 2, title: "Переезд"},
	{id: 3, title: "Строительные материалы"},
	{id: 4, title: "Двери"},
	{id: 5, title: "Мебель"},
	{id: 6, title: "Техника"},
	{id: 7, title: "Кровати"},
	{id: 8, title: "Вещи"},
	{id: 9, title: "Дачный переезд"},
	{id: 10, title: "Переезд"},
	{id: 11, title: "Строительные материалы"},
	{id: 12, title: "Двери"},
	{id: 13, title: "Мебель"},
	{id: 14, title: "Техника"},
	{id: 15, title: "Кровати"},
	{id: 16, title: "Вещи"},
]
</script>

<template>
<section id="delivery">
	<TheContainer class="flex-col bg-white">
	<h2 class="text-4xl font-semibold">Разная доставка для разных задач</h2>
	<UILabelContainer class="gap-3">
		<UILabelItem
		v-for="label of labels" :key="label.id"
		class="bg-gray-50 font-medium"
		>
			{{ label.title }}
		</UILabelItem>
	</UILabelContainer>
</TheContainer>
</section>

</template> -->
