<script setup>
import { shallowRef } from 'vue';
import Main from './components/Main.vue'
import { SunIcon, MoonIcon } from '@heroicons/vue/16/solid'
import Sobre from './components/Conteudo/Sobre.vue'
import Experiencias from './components/Conteudo/Experiencias.vue'
import Contato from './components/Conteudo/Contato.vue'
import About from './components/Conteudo/About.vue';


const darkMode = shallowRef(true);

const chageTheme = () => {
  darkMode.value = !darkMode.value;
}

const myVar = shallowRef();

function myFunction() {
  myVar.value = setTimeout(showPage, 3000);
}

function showPage() {
  document.getElementById("loader").style.display = "none";
  document.getElementById("mainDiv").style.display = "block";
}

</script>

<template>
  <div id="loader" class="h-screen flex bg-gray-800">
    {{ myFunction() }}
   <div class="text-center mx-auto flex sm:pt-32 text-pink-500 text-4xl font-mono font-medium">
    <span class="let1">N</span>  
    <span class="let2">I</span>  
    <span class="let3">C</span>  
    <span class="let4">O</span>  
    <span class="let5">L</span>  
    <span class="let6">E</span>   
    <span class="let2 ml-5">W</span>  
    <span class="let3">E</span>  
    <span class="let4">B</span>    
    <span class="let6 ml-5">D</span>  
    <span class="let6">E</span>  
    <span class="let6">V</span>  
   </div>
  </div>
  <div id="mainDiv">
    <div>
      <header>
        <nav
          :class="darkMode == true ? 'border-gray-200 px-4 lg:px-6 py-2.5 dark:bg-gray-800 border-b-pink-500   border-b-2' : 'border-gray-200 px-4 lg:px-6 py-2.5 bg-pink-100 border-b-pink-500   border-b-2'">
          <div class="  py-3 flex flex-wrap justify-between items-center mx-auto sm:px-8 px-2">
            <a href="/" class="flex items-center">
              <img src="./assets/img/logo.png" class="mr-3 h-8 sm:h-16" alt="Logo" />
            </a>
            <div class="flex items-end">
              <button data-collapse-toggle="mobile-menu-2" type="button"
                class="inline-flex items-center p-2 ml-1 text-sm text-gray-500 rounded-lg lg:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
                aria-controls="mobile-menu-2" aria-expanded="false">
                <span class="sr-only">Open main menu</span>
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd"
                    d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                    clip-rule="evenodd"></path>
                </svg>
                <svg class="hidden w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd"
                    d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                    clip-rule="evenodd"></path>
                </svg>
              </button>
            </div>
            <div class="hidden justify-between items-center w-full lg:flex lg:w-auto lg:order-1" id="mobile-menu-2">
              <ul class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0">
                <li class="animate-bottom">
                  <a href="#sobre"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">Sobre</a>
                </li>
                <li class="animate-bottom">
                  <a href="#experiencias"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">Experiências</a>
                </li>
                <li class="animate-bottom">
                  <a href="#contatos"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">Contato</a>
                </li>
                <li class="animate-bottom">
                  <div @click="chageTheme()"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">
                    <MoonIcon v-if="darkMode == false" class="text-black w-8 h-8  cursor-pointer" />
                    <SunIcon v-if="darkMode == true" class="text-pink-500 w-8 h-8  cursor-pointer" />
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </header>
    </div>
    <main class="scroll-container">
      <Sobre class="scroll-page" :darkMode="darkMode" id="main" />
      <About class="scroll-page" :darkMode="darkMode" id="sobre" />
      <Experiencias class="scroll-page" :darkMode="darkMode" id="experiencias" />
      <Contato class="scroll-page" :darkMode="darkMode" id="contatos" />
    </main>
  </div>
</template>

<style scoped>
span {
  position: relative;
  top: 0.63em;  
  display: inline-block;
  text-transform: uppercase;  
  opacity: 0;
  transform: rotateX(-90deg);
}

.let1 {
  animation: drop 1.2s ease-in-out infinite;
  animation-delay: 1.2s;
}

.let2 {
  animation: drop 1.2s ease-in-out infinite;
  animation-delay: 1.3s;
}

.let3 {
  animation: drop 1.2s ease-in-out infinite;
  animation-delay: 1.4s;
}

.let4 {
  animation: drop 1.2s ease-in-out infinite;
  animation-delay: 1.5s;

}

.let5 {
  animation: drop 1.2s ease-in-out infinite;
  animation-delay: 1.6s;
}

.let6 {
  animation: drop 1.2s ease-in-out infinite;
  animation-delay: 1.7s;
}

.let7 {
  animation: drop 1.2s ease-in-out infinite;
  animation-delay: 1.8s;
}

@keyframes drop {
    10% {
        opacity: 0.5;
    }
    20% {
        opacity: 1;
        top: 3.78em;
        transform: rotateX(-360deg);
    }
    80% {
        opacity: 1;
        top: 3.78em;
        transform: rotateX(-360deg);
    }
    90% {
        opacity: 0.5;
    }
    100% {
        opacity: 0;
        top: 6.94em
    }
}


#mainDiv {
  display: none;
}
.animate-bottom {
  position: relative;
  -webkit-animation-name: animatebottom;
  -webkit-animation-duration: 1s;
  animation-name: animatebottom;
  animation-duration: 1s
}

@-webkit-keyframes animatebottom {
  from { right:-50px; opacity:0 } 
  to { right:0px; opacity:1 }
}

@keyframes animatebottom { 
  from{ right:-50px; opacity:0 } 
  to{ right:0; opacity:1 }
}


</style>


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




