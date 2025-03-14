<script setup lang="ts">

const {imgSrc, title, description} = defineProps<{
    imgSrc: string
    title: string
    description: string
}>()

</script>

<template>
    <article class="flex p-3 justify-between items-center rounded-2xl bg-gray-50 [&_header]:hover:text-white ">
        <header class="flex items-center gap-5">
            <img class="mt-2 h-10 rounded-full" :src="imgSrc" :alt="title">
            <div>
                <h2 class="text-xl font-semibold">{{ title }}</h2>
                <p class="opacity-90">{{ description }}</p>
            </div>
        </header>
        <IconsArrow class="h-8 [&_.circle-fill]:text-white [&_.circle-stroke]:text-current [&_.arrow]:text-black"/>
    </article>
</template>

<!-- <Icon :name="iconName" size="5rem" mode="svg"></Icon> -->