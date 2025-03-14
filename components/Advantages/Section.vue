<template>
    <section id="advantages" class="flex">
        <TheContainer class="flex-col w-max-full bg-white">
            <h2 class="text-4xl font-semibold">Преимущества</h2>
            <div class="flex sm:grid grid-cols-2 grid-rows-2 justify-evenly flex-wrap gap-2">
                <AdvantagesArticle
                title="Скорость"
                description="Доставим груз в установленный срок"
                icon-name="material-symbols-light:delivery-truck-speed-outline-rounded"
                class="hover:bg-blue-600 hover:text-white transition-colors"
                />
                <AdvantagesArticle
                title="Логистика"
                description="Развитая инфраструктура логистических пунктов"
                icon-name="material-symbols-light:conversion-path"
                class="hover:bg-pink-600 hover:text-white transition-colors"
                />
                <AdvantagesArticle
                title="Надёжность"
                description="Заключим договор и предоставим страховку груза"
                icon-name="material-symbols-light:handshake-outline-sharp"
                class="hover:bg-purple-600 hover:text-white transition-colors"
                />
                <AdvantagesArticle
                title="Сохранность"
                description="Гарантируем доставку в полной сохранности"
                icon-name="material-symbols-light:package-2-outline"
                class="hover:bg-fuchsia-600 hover:text-white transition-colors"
                />
            
            </div>
        </TheContainer>
    </section>
    
</template>

