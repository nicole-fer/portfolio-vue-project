<script setup>
const props = defineProps({
    darkMode: Boolean,
});
</script>

<template>
    <div :class="darkMode == true
            ? 'pt-12 bg-gray-800 flex justify-center'
            : 'pt-12 bg-pink-100 flex justify-center'
        ">
        <div class="sm:w-1/2">
            <div class="text-center h-10/12">
                <p :class="darkMode == true
                        ? 'text-pink-500 font-mono text-lg font-medium'
                        : 'text-pink-600 font-mono text-lg  font-medium'
                    ">
                    Se interessou?
                </p>
                <p :class="darkMode == true
                        ? 'text-5xl text-gray-200 mt-2 font-semibold'
                        : 'font-medium text-5xl text-gray-700 mt-2'
                    ">
                    Entre em Contato
                </p>
                <p>
                    Caso queira entrar em contato, conecte-se comigo nas redes sociais. Estou pronta para criar novas experiências!"
                </p>
            </div>
            <div :class="darkMode == true
                    ? 'text-white text-sm font-mono pb-4 h-2/12'
                    : 'text-center text-sm font-mono pb-4'
                ">
                <div class="text-center">
                    <p class="self-end">Desenvolvido por Nicole Fernandes</p>
                    <p class="self-end">2024</p>
                </div>
            </div>
        </div>
    </div>
</template>