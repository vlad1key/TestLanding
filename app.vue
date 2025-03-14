<script setup>
	useHead({
		bodyAttrs: {
			class: "bg-gray-50"
		}
	})
</script>

<template>
	<NuxtLayout>
		<NuxtPage/>
	</NuxtLayout>
</template>

<style>
@import "~/assets/css/main.css";


html{ scroll-behavior: smooth; }

html,
body,
#__nuxt
{
height: 100%;
}
</style>
