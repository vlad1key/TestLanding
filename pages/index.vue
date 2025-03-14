<script setup lang="ts">
definePageMeta({
	layout: "landing",
});
</script>

<template>
    <div class="flex flex-col justify-between w-full gap-5">
	    <AdvantagesSection/>
	    <ServicesSection/>
		<AboutSection/>
		<TruckFleetSection/>
		<DeliverySection/>
		<FaqSection/>
		<ContactSection/>
    </div>

</template>
