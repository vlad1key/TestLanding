<template>
    <section id="services" class="flex">
        <TheContainer class="flex-col sm:flex-row justify-between bg-white">
            <h2 class="text-4xl font-semibold">Наши услуги</h2>
            <div class="flex flex-col flex-grow gap-2">    
                <ServicesArticle 
                title="Название услуги" 
                description="Описание услуги" 
                imgSrc="/service.png"
                class="hover:bg-blue-500 transition-colors"
                />
                <ServicesArticle 
                title="Название услуги" 
                description="Описание услуги" 
                imgSrc="/service.png"
                class="hover:bg-cyan-500 transition-colors"
                />
                <ServicesArticle 
                title="Название услуги" 
                description="Описание услуги" 
                imgSrc="/service.png"
                class="hover:bg-pink-500 transition-colors"
                />
                <ServicesArticle 
                title="Название услуги" 
                description="Описание услуги" 
                imgSrc="/service.png"
                class="hover:bg-purple-600 transition-colors"
                />
            
            </div>
        </TheContainer>
       
    </section>
    
</template>
