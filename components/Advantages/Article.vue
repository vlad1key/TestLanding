<script setup lang="ts">

const {iconName, title, description} = defineProps<{
    iconName: string
    title: string
    description: string
}>()

</script>

<template>
    <article class="flex flex-col flex-grow p-3 justify-between gap-10 rounded-2xl bg-gray-50">
        <header class="flex flex-col">
            <Icon :name="iconName" size="5rem" mode="svg"></Icon>
            <h2 class="text-xl font-semibold">{{ title }}</h2>
        </header>
        <p class="opacity-80">{{ description }}</p>
    </article>
</template>