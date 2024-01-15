<script setup>
const props = defineProps({
    darkMode:Boolean,
    propsLanguage: Object
})
</script>

<template>
        <div :class=" darkMode==true ? 'border-t-4 border-pink-500 bg-gray-800 sm:pr-20 pr-4  sm:grid sm:grid-cols-7 sm:place-content-between' : 'bg-pink-100  sm:pr-20 pr-4  sm:grid sm:grid-cols-7  sm:place-content-between text-gray-800 border-t-4 border-pink-500'">
            <div class="flex place-items-end  sm:col-span-3">
                <img class="sm:mt-16 w-11/12" src="../../assets/img/imagem.png"/>
            </div>
            <div class="sm:col-span-4">
               <div class="sm:mt-24 px-3 mt-6">
                <p class="text-4xl text-pink-500 font-mono font-bold" >{{ propsLanguage.about.sobre }}</p>
                <p :class="darkMode==true ? 'sm:text-lg text-pink-100 text-justify mt-2 sm:pb-32 pb-8' : 'sm:pb-32 pb-8 sm:text-lg text-gray-800 text-justify mt-2'">
                   {{ propsLanguage.about.apresentacao }}
                </p>
               </div>
            </div>
        </div>
</template>