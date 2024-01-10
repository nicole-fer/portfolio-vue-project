<script setup>
const props = defineProps({
    darkMode: Boolean
})
</script>

<template>
    <div :class="darkMode == true ? 'grid grid-cols-5  text-white h-screen bg-gradient-to-b from-gray-800 to-cyan-800' : 'bg-gradient-to-b from-pink-100 to-pink-200  grid grid-cols-5 h-screen'">
        <div class="sm:px-8	flex place-items-center col-span-3 sm:mr-12">
          <div class="sm:-mt-64">
            <p :class=" darkMode==true  ? 'text-7xl font-mono font-medium text-pink-400' : 'text-7xl font-mono font-medium text-pink-600'">Olá! Me chamo Nicole Fernandes</p>
            <p :class="darkMode==true ? 'text-4xl text-justify text-pink-200': 'text-4xl text-justify text-blue-950'">Sou desenvolvedora web e graduada em Engenharia da Computação pela Universidade Federal do Ceará (UFC). Seja bem vindo(a) ao meu portifólio.</p>
          </div>
        </div>
        <div class="sm:-mt-12 place-items-center col-span-2 flex justify-end">
            <img class="h-2/3 w-3/5" src="../../assets/img/icon.png"/>
        </div>
    </div>
</template>