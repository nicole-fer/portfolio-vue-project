<script setup>
const props = defineProps({
    darkMode:Boolean
})
</script>

<template>
        <div :class=" darkMode==true ? 'border-t-4 border-pink-500 bg-gray-800 pl-4 sm:pl-0  sm:pr-20 pr-4  sm:grid grid-cols-8 sm:gap-4 sm:place-content-between h-screen' : 'bg-pink-100 h-screen pl-4 sm:pl-0 sm:pr-20 pr-4  sm:grid grid-cols-8 sm:gap-4 sm:place-content-between text-gray-800 border-t-4 border-pink-500'">
            <div class="flex place-items-center pl-4 sm:relative sm:col-span-3">
             Imagem
            </div>
            <div class="flex place-items-center sm:col-span-5 ">
               <div>
                <p class="text-4xl text-orange-500 font-mono font-bold " >Sobre mim</p>
                <p :class="darkMode==true ? 'sm:text-xl text-lg text-orange-100 text-justify mt-2' : 'sm:text-xl text-lg text-gray-800 text-justify mt-2'">Seja bem-vindo ao meu portfólio! Meu nome é Nicole Fernandes, tenho 23 anos e sou uma desenvolvedora web com foco no front-end. Atualmente, estou no finalzinho da minha graduação em Engenharia da Computação, na Universidade Federal do Ceará (UFC). </p>
                <p :class="darkMode==true ? 'sm:text-xl text-lg text-orange-100 text-justify mt-2' : 'sm:text-xl text-lg text-gray-800 text-justify mt-2'"> Possuo conhecimento em tecnologias, como Javascript, Typescript, HTML, CSS, React JS, Vue JS e React Native, para mobile. Além disso, já trabalhei com conexões de backend nas tecnologias Laravel e Sprintboot e com bibliotecas como InertiaJS, Tailwind CSS e Ant Design.</p>
                <p :class="darkMode==true ? 'sm:text-xl text-lg text-orange-100 text-justify mt-2' : 'sm:text-xl text-lg text-gray-800 text-justify mt-2'">Sempre busco novos desafios e oportunidades para aprimorar meus conhecimentos e habilidades, e estou disponível para projetos de desenvolvimento web e mobile. Além disso, gosto de ir ao cinema e viajar em família, buscando equilibrar minha vida profissional e pessoal.</p>
                <p :class="darkMode==true ? 'sm:text-xl text-lg text-orange-100 text-justify mt-2' : 'sm:text-xl text-lg text-gray-800 text-justify mt-2'">Aqui neste portfólio, você encontrará uma amostra dos meus trabalhos mais recentes e projetos desenvolvidos, com o objetivo de demonstrar minhas habilidades na área. Sinta-se à vontade para explorar e entrar em contato comigo para discutir possíveis oportunidades de trabalho juntos!</p>
               </div>
            </div>
        </div>
</template>