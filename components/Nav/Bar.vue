

<template>
	<TheContainer class="h-12 w-full px-6 bg-white">
		<ul class="flex flex-grow justify-between items-center h-1/2">
			<li><NuxtLink to="#about">О нас</NuxtLink></li>
			<li><NuxtLink to="#services">Услуги</NuxtLink></li>
			<li><NuxtLink to="#contacts">Контакты</NuxtLink></li>
			<li><NuxtLink to="#workstages">Этапы работ</NuxtLink></li>
			<li><NuxtLink to="#faq">FAQ</NuxtLink></li>
		</ul>
		<ButtonComponent class="btn bg-black"/>
	</TheContainer>
</template>

<style scoped>
@media screen and (max-width: 868px) {
	.btn{
		display: none;
	}
}

ul>li{
display: flex;
justify-content: center;
align-items: center;
}
li > * {
	 text-wrap-mode: nowrap;
}
</style>

