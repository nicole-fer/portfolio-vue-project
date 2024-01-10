<script setup>
import { shallowRef } from 'vue';
import Main from './components/Main.vue'
import  { SunIcon, MoonIcon } from '@heroicons/vue/16/solid' 
import Sobre from './components/Conteudo/Sobre.vue'
import Experiencias from './components/Conteudo/Experiencias.vue'
import Contato from './components/Conteudo/Contato.vue'
import About from './components/Conteudo/About.vue';


const darkMode = shallowRef(false);

const chageTheme = () =>  {
  darkMode.value = !darkMode.value;
}

</script>

<template>
  <div>
      <div>
        <header>
    <nav :class="darkMode==true ? 'border-gray-200 px-4 lg:px-6 py-2.5 dark:bg-gray-800 border-b-pink-500   border-b-2' : 'border-gray-200 px-4 lg:px-6 py-2.5 bg-pink-100 border-b-pink-500   border-b-2'">
        <div class="  py-3 flex flex-wrap justify-between items-center mx-auto sm:px-8 px-2">
            <a href="https://flowbite.com" class="flex items-center">
                <img src="./assets/img/logo.png" class="mr-3 h-8 sm:h-16" alt="Flowbite Logo" />
            </a>
            <div class="flex items-end">
                <button data-collapse-toggle="mobile-menu-2" type="button" class="inline-flex items-center p-2 ml-1 text-sm text-gray-500 rounded-lg lg:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="mobile-menu-2" aria-expanded="false">
                    <span class="sr-only">Open main menu</span>
                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
                    <svg class="hidden w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                </button>
            </div>
            <div class="hidden justify-between items-center w-full lg:flex lg:w-auto lg:order-1" id="mobile-menu-2">
                <ul class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0">
                    <li>
                        <a href="#sobre" :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">Sobre</a>
                    </li>
                    <li>
                        <a href="#experiencias" :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">Experiências</a>
                    </li>
                    <li>
                        <a href="#contatos" :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">Contato</a>
                    </li>
                    <li>
                        <div @click="chageTheme()" :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'"> 
                          <MoonIcon v-if="darkMode==false" class="text-black w-8 h-8  cursor-pointer"/> 
                          <SunIcon v-if="darkMode==true" class="text-pink-500 w-8 h-8  cursor-pointer"/> 
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</header>
      </div>
    <main id="scroll-container">
     <Sobre class="scroll-page" id="main" :darkMode="darkMode"/>
     <About class="scroll-page" id="sobre" :darkMode="darkMode"/>
     <Experiencias class="scroll-page" id="experiencias"/>
     <Contato class="scroll-page" id="contatos"/>
    </main>
  </div>
</template>


<style module>
a {
  display: inline-block;
  text-decoration: none;
}
nav,
.scroll-container {
  display: block;
  text-align: center;
}
nav {
  width: full;
}
.scroll-container {
  overflow-y: scroll;
  scroll-behavior: smooth;
}
.scroll-page {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  font-size: 5em;
}
</style>




