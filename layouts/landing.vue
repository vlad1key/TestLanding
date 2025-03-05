

<template>
	<div id="landing" class="flex flex-col justify-center items-center min-h-full px-32">
		<header class="w-full">
			<div class="absolute top-0 left-0 -z-10 w-screen h-screen aspect-video bg-cover bg-center bg-no-repeat bg-[url(/public/truck-1.webp)]"></div>
			<NavBar class="mt-9"/>
			
		</header>
			
		<main class="flex-grow w-full h-full">
			<slot />
		</main>
		<footer class="w-full">
			<NavBar />
		</footer>
	</div>
</template>
