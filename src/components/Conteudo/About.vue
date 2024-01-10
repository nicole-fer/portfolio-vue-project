<script setup>
const props = defineProps({
    darkMode:Boolean
})
</script>

<template>
        <div :class=" darkMode==true ? 'border-t-4 border-pink-500 bg-gray-800 sm:pr-20 pr-4  sm:grid grid-cols-7 sm:place-content-between' : 'bg-pink-100  sm:pr-20 pr-4  sm:grid grid-cols-7  sm:place-content-between text-gray-800 border-t-4 border-pink-500'">
            <div class="flex place-items-end  sm:col-span-3">
                <img class="sm:mt-16 w-full" src="../../assets/img/imagem.png"/>
            </div>
            <div class="sm:col-span-4">
               <div class="sm:mt-48">
                <p class="text-5xl text-pink-500 font-mono font-bold" >Sobre mim</p>
                <p :class="darkMode==true ? 'sm:text-2xl text-lg text-pink-100 text-justify mt-2 pb-32' : 'pb-32 sm:text-2xl text-lg text-gray-800 text-justify mt-2'">
                    Seja bem-vindo ao meu portfólio! Meu nome é Nicole Fernandes, tenho 23 anos e sou uma desenvolvedora web com foco no front-end. Atualmente, estou no finalzinho da minha graduação em Engenharia da Computação, na Universidade Federal do Ceará (UFC).
                    Possuo conhecimento em tecnologias, como Javascript, Typescript, HTML, CSS, React JS, Vue JS e React Native, para mobile. Além disso, já trabalhei com conexões de backend nas tecnologias Laravel e Sprintboot e com bibliotecas como InertiaJS, Tailwind CSS e Ant Design.
                    Sempre busco novos desafios e oportunidades para aprimorar meus conhecimentos e habilidades, e estou disponível para projetos de desenvolvimento web e mobile. Além disso, gosto de ir ao cinema e viajar em família, buscando equilibrar minha vida profissional e pessoal.
                    Aqui neste portfólio, você encontrará uma amostra dos meus trabalhos mais recentes e projetos desenvolvidos, com o objetivo de demonstrar minhas habilidades na área. Sinta-se à vontade para explorar e entrar em contato comigo para discutir possíveis oportunidades de trabalho juntos!
                </p>
               </div>
            </div>
        </div>
</template>