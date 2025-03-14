<template>

  <div id="landing" class="flex flex-col px-1 max-w-4xl sm:px-5 mx-auto w-full">
		<header class="flex flex-col w-full h-screen">
			<div class="absolute top-0 left-0 -z-10 w-screen h-screen bg-cover bg-center bg-no-repeat bg-[url(/public/truck-1.webp)]"></div>
			<NavBar/>
			<div id="offer" class="flex justify-end items-start h-full flex-col pb-[10vh]">
		  		<TheContainer class="flex-col gap-5 !w-[clamp(15rem,45vw,28rem)] mt-15 bg-white">
					<div class="flex flex-col gap-2">
						<h1 class="text-4xl font-bold">Перевозка грузов<br>по всей России</h1>
						<p class="">Перевозим негабаритные и тяжеловесные&nbsp;грузы</p>
					</div>
					<a href="#contact"><UIButtonComponent class="h-10" title="Заказать доставку"/></a>
				</TheContainer>
			</div>
		</header>
			
		<main class="flex flex-col justify-between flex-grow h-full gap-6 w-full">
			<slot></slot>
		</main>
		<footer class="w-full">
			<NavBar/>
		</footer>
  </div>
</template>


