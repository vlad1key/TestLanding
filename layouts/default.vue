<template>
	<div class="flex flex-col justify-center items-center">
		<header>
            <NavBar />
        </header>
		<main class="flex-grow">
            <slot/>
        </main>
		<footer>
			<p>footer</p>
			<NavBar />
		</footer>
	</div>
</template>
