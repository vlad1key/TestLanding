<script setup lang="ts">
import type { Dimension } from './Carousel.vue'

type FormData = {
    name: string
    phone: string
    serviceType: string
    dimension?: Dimension
}

const form = reactive<FormData>({
    name: "",
    phone: "",
    serviceType: "",   
})

const submitForm = () => {
	alert(`
    Введённые данные: 
    Имя: ${form.name}
    Телефон: ${form.phone}
    Вид услуги: ${form.serviceType}
    Габариты: ${form.dimension?.xyz.join(" x ")}
    `);
};
</script>

<template>
	<section id="contact" class="flex">
		<TheContainer class="justify-between flex-col md:flex-row bg-white">
			<div class="flex flex-1 flex-col gap-5">
				<h2 class="text-4xl font-semibold">
					Свяжитесь с&nbsp;нами
				</h2>

				<div class="flex flex-col justify-between font-medium gap-3">
					<div class="flex items-center gap-2">
						<Icon
							name="solar:phone-outline"
							mode="svg"
							size="1.3rem"
							class="text-blue-700"
						/>
						<a href="tel:+78612051535" class="hover:text-blue-700"
							>+7 (861) 205-15-35</a
						>
					</div>
					<div class="flex items-center gap-2">
						<Icon
							name="material-symbols:mail-outline"
							mode="svg"
                            size="1.3rem"
							class="text-blue-700"
						/>
						<a href="mailto:info@m2partner.ru" class="hover:text-blue-700"
							>info@m2partner.ru</a
						>
					</div>
					<div class="flex items-center gap-2">
                        <!-- todo: исправить положение иконки (длинный текст растягивает контейнер и иконка съезжает с центра) -->
						<Icon name="bi:geo-alt" size="1.3rem" class="text-blue-700" />
						<address>
							350090, г. Краснодар ул. Стахановская 1/3 С1, 2 этаж, офис 207
						</address>
					</div>
				</div>
			</div>
			<div class="flex flex-1 flex-col justify-center gap-5">
				<h3 class="text-lg font-semibold leading-5">
					Заполните эту форму.<br />Мы свяжемся с вами и рассчитаем стоимость.
				</h3>
				<form
					@submit.prevent="submitForm"
					class="flex flex-col gap-3 [&_input]:px-2 [&_input]:py-1 [&_input]:w-full [&_input]:border [&_input]:rounded-lg"
				>
					<div class="relative w-full">
						<input 
						v-model="form.name" 
						type="text" 
						placeholder="Ваше имя" 
						class="border-gray-300 placeholder:text-sm text-sm placeholder:font-medium placeholder:opacity-80"
						required
						/>
						<Icon
						v-if="form.name"
						name="bxs:trash"
						mode="svg"
						class="absolute right-3 top-1/2 -translate-y-1/2 cursor-pointer opacity-60 hover:text-red-600"
						@click="form.name = ''"
						/>
					</div>
					<div class="relative w-full">
						<input
						v-model="form.phone"
						type="tel"
						placeholder="Ваш номер"
						class="border-gray-300 placeholder:text-sm text-sm placeholder:font-medium placeholder:opacity-80"
						required
						/>
						<Icon
						v-if="form.phone"
						name="bxs:trash"
						mode="svg"
						class="absolute right-3 top-1/2 -translate-y-1/2 cursor-pointer opacity-60 hover:text-red-600"
						@click="form.phone = ''"
						/>
					</div>
					<div class="relative w-full">
						<input 
						v-model="form.serviceType" 
						placeholder="Вид услуги" 
						class="border-gray-300 placeholder:text-sm text-sm placeholder:font-medium placeholder:opacity-80"
						required 
						/>
						<Icon
						v-if="form.serviceType"
						name="bxs:trash"
						mode="svg"
						class="absolute right-3 top-1/2 -translate-y-1/2 cursor-pointer opacity-60 hover:text-red-600"
						@click="form.serviceType = ''"
						/>
					</div>
					<ContactCarousel @select=" d => form.dimension = d "></ContactCarousel>

					<UIButtonComponent class="h-10" title="Отправить"/>
				</form>
			</div>
		</TheContainer>
	</section>
</template>

<!----------------------------------------------------------------------->

<!-- <script setup lang="ts">

const contactSubmit = function(){

}
</script>

<template>

	<section id="contact" class="flex">
		<TheContainer class="bg-white">
			<div class="flex flex-col">
				<h2>Свяжитесь с нами</h2>
				<address class="flex flex-col justify-between">
					<div>
						<Icon name="solar:phone-outline"/><a href="tel:+78612051535">+7 (861) 205-15-35</a>
					</div>
					<div>
						<Icon name="material-symbols:mail-outline"/><a href="mailto:info@m2partner.ru">info@m2partner.ru</a>
					</div>
					<div>
						<Icon name="bi:geo-alt"/><a href="geo:45.072217,38.969429">350090, г. Краснодар ул. Стахановская 1/3 С1, 2 этаж, офис 207</a>
					</div>
				</address>
			</div>
			<form @submit.prevent>
				<h3>Заполните эту форму. <br> Мы свяжемся с вами и рассчитаем стоимость.</h3>
				<UIButtonComponent title="Отправить"></UIButtonComponent>
			</form>
			
		</TheContainer>
	</section>
</template> -->
