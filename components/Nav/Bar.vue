
<template>
	<TheContainer id="nav" class="gap-5 justify-between items-center h-12 my-7 w-full bg-white">
		<ul class="flex flex-grow gap-[2vw]">
			<li><NuxtLink to="#about">О нас</NuxtLink></li>
			<li><NuxtLink to="#services">Услуги</NuxtLink></li>
			<li><NuxtLink to="#contact">Контакты</NuxtLink></li>
			<!-- <li><NuxtLink to="#workstages">Этапы работ</NuxtLink></li> -->
			<li><NuxtLink to="#faq">FAQ</NuxtLink></li>
		</ul>
		<UIButtonComponent title="Заказать доставку" class="btn h-8"/>
	</TheContainer>
</template>

<style scoped>

ul>li{
  display: flex;
  justify-content: center;
  align-items: center;
  text-wrap: nowrap;
}

@media screen and (max-width: 681px) {
	.btn{
		display: none;
	}
	ul{
		justify-content: space-between;
	}
}


</style>

