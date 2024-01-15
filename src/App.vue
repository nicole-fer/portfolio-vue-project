<script setup>
import { computed, shallowRef, ref } from 'vue';
import Main from './components/Main.vue'
import { SunIcon, MoonIcon } from '@heroicons/vue/16/solid'
import Sobre from './components/Conteudo/Sobre.vue'
import Experiencias from './components/Conteudo/Experiencias.vue'
import Contato from './components/Conteudo/Contato.vue'
import About from './components/Conteudo/About.vue';


const darkMode = shallowRef(true);

const port = {
  sobre: {
    nome: 'Olá! Me chamo Nicole Fernandes',
    apresentacao: 'Sou desenvolvedora web e graduada em Engenharia da Computação pela Universidade Federal do Ceará (UFC). Seja bem vindo(a) ao meu portifólio.'
  },
  header: {
    sobre: 'Sobre',
    exp: 'Experiências',
    contato: 'Contato',
  },
  about: {
    sobre: 'Sobre mim',
    apresentacao: 'Olá! Sou Nicole Fernandes, tenho 24 anos e sou apaixonada por tecnologia. Concluí minha formação em Engenharia da Computação na Universidade Federal do Ceará (UFC), onde desenvolvi uma base sólida e abrangente em minha área de atuação. Além de minha dedicação ao mundo da programação, tenho um grande amor por viagens em família. Explorar novos destinos e criar memórias inesquecíveis com aqueles que amo é algo que realmente me completa. Quando não estou planejando minha próxima aventura, você pode me encontrar assistindo animes, filmes e séries. Essas são paixões que alimentam minha imaginação e me permitem relaxar após longas horas de trabalho. Profissionalmente, já trilhei caminhos tanto no desenvolvimento Frontend quanto Fullstack, na seção experiências, mostro todas as tecnologias com que já trabalhei. Essa versatilidade me proporcionou uma compreensão abrangente do desenvolvimento de software, desde a criação de interfaces atraentes até a implementação de funcionalidades complexas nos bastidores. Acredito que a combinação de minha formação acadêmica e experiência profissional me permite abordar os desafios com criatividade e soluções inovadoras. Espero que, ao conhecer um pouco mais sobre mim, você perceba a minha paixão pelo que faço e o comprometimento que tenho em oferecer resultados excepcionais. Estou sempre em busca de novos conhecimentos e desafios que me permitam crescer tanto pessoal quanto profissionalmente. Seja bem-vindo ao meu universo, e estou ansiosa para contribuir de forma significativa em projetos futuros!'
  },
  exp: {
    titulo: 'Experiências',
    tec: 'Tecnologias Usadas:',
    exps: [
      {
        titulo: 'Prefeitura Municipal de Sobral',
        descricao: 'Estágio de 6 meses em Engenharia da Computação na Secretária da Saúde, como programadora, contribuindo para o desenvolvimento de aplicativos web. Envolvi-me em algumas fases do ciclo de vida do software, como concepção e implementação, mas com foco especial em melhorias de softwares já existentes.',
        data: 'Maio 2022',
        atividade: 'Estágio em Engenharia da Computação'
      }, {
        titulo: 'GREAT',
        descricao: 'Atuação como programadora FrontEnd Jr, por 5 meses. Colaborei na criação de interfaces intuitivas, responsivas e visualmente atraentes. Contribuí para aprimorar a experiência do usuário, trabalhando em conjunto com a equipe para implementar novos recursos e otimizar o desempenho.',
        data: 'Outubro 2022',
        atividade: 'Desenvolvedora FrontEnd Jr'
      }, {
        titulo: 'Grupo PluralMed',
        descricao: 'Experiência como programador FullStack, durante 8 meses, liderando o desenvolvimento completo de dois módulos críticos, com foco em Atenção Especializada e Internação Hospitalar. Responsável por arquitetar soluções integradas, desde o backend até a interface do usuário. Além disso, contribuí ativamente para a implementação e melhorias em softwares já existentes, assegurando a coesão e aprimoramento contínuo do sistema. Colaborei na criação de recursos avançados, garantindo eficiência operacional e qualidade no atendimento hospitalar.',
        data: 'Junho 2022',
        atividade: 'Desenvolvedora FullStack'
      }
    ]
  },
  contato:{
    interesse: 'Se interessou?',
    contato: 'Entre em Contato',
    descricao: 'Caso queira entrar em contato, conecte-se comigo nas redes sociais. Estou pronta para criar novas experiências!',
    footer: 'Desenvolvido por Nicole Fernandes'
  }
}


const ingles = {
  sobre: {
    nome: 'Hello! My name is Nicole Fernandes',
    apresentacao: 'I am a web developer and graduated in Computer Engineering from the Federal University of Ceará (UFC). Welcome to my portfolio.'
  },
  header: {
    sobre: 'About',
    exp: 'Experiences',
    contato: 'Contact',
  },
  about: {
    sobre: 'About me',
    apresentacao: "Hello! I am Nicole Fernandes, 24 years old, and passionate about technology. I completed my degree in Computer Engineering at the Federal University of Ceará (UFC), where I developed a solid and comprehensive foundation in my field. In addition to my dedication to the programming world, I have a great love for family travel. Exploring new destinations and creating unforgettable memories with those I love truly fulfills me. When I'm not planning my next adventure, you can find me watching anime, movies, and series. These are passions that fuel my imagination and allow me to relax after long hours of work. Professionally, I have navigated paths in both Frontend and Fullstack development. In the experiences section, I showcase all the technologies I have worked with. This versatility has provided me with a comprehensive understanding of software development, from creating attractive interfaces to implementing complex functionalities behind the scenes. I believe that the combination of my academic background and professional experience allows me to approach challenges with creativity and innovative solutions. I hope that by learning a bit more about me, you can sense my passion for what I do and the commitment I have to deliver exceptional results. I am always seeking new knowledge and challenges that allow me to grow both personally and professionally. Welcome to my universe, and I look forward to contributing meaningfully to future projects!"
  }, 
  exp: {
    titulo: 'Experiences',
    tec: 'Technologies Used:',
    exps: [
      {
        titulo: 'Sobral City Hall',
        descricao: 'Six-month internship in Computer Engineering at the Health Department, working as a programmer and contributing to the development of web applications. Involved in various stages of the software lifecycle, including conception and implementation, with a special focus on enhancing existing software.',
        data: 'May 2022',
        atividade: 'Internship in Computer Engineering'
      }, {
        titulo: 'GREAT',
        descricao: 'Worked as a Junior FrontEnd Developer for 5 months. Collaborated on creating intuitive, responsive, and visually appealing interfaces. Contributed to enhancing the user experience by working closely with the team to implement new features and optimize performance.',
        data: 'October 2022',
        atividade: 'Junior FrontEnd Developer'
      }, {
        titulo: 'PluralMed Group',
        descricao: 'Experience as a FullStack Developer for 8 months, leading the complete development of two critical modules focused on Specialized Care and Hospitalization. Responsible for architecting integrated solutions from backend to user interface. Additionally, actively contributed to implementing and improving existing software, ensuring cohesion and continuous system enhancement. Collaborated in creating advanced features, ensuring operational efficiency and quality in hospital care..',
        data: 'June 2022',
        atividade: 'FullStack Developer'
      }
    ]
  },
  contato:{
    interesse: 'Interested?',
    contato: 'Get in touch.',
    descricao: "If you want to get in touch, connect with me on social media. I'm ready to create new experiences.!",
    footer: 'Developed by Nicole Fernandes'
  }
}


const language = shallowRef(true)
const propsLanguage = shallowRef(port)

const chageLanguage = () => {
  language.value = !language.value
  language.value == true ? propsLanguage.value = port : propsLanguage.value = ingles
}

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
          :class="darkMode == true ? 'border-gray-200 px-4 lg:px-6 py-2.5 bg-gray-800 border-b-pink-500 border-b-2' : 'border-gray-200 px-4 lg:px-6 py-2.5 bg-pink-100 border-b-pink-500   border-b-2'">
          <div class="  py-3 flex flex-wrap justify-between items-center mx-auto sm:px-8 px-2">
            <a href="/" class="flex items-center">
              <img src="./assets/img/logo.png" class="mr-3 h-8 sm:h-16" alt="Logo" />
            </a>
            <div class="hidden justify-between items-center w-full lg:flex lg:w-auto lg:order-1">
              <ul class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0">
                <li class="animate-bottom">
                  <a href="#sobre"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">{{
                      propsLanguage.header.sobre }}</a>
                </li>
                <li class="animate-bottom">
                  <a href="#experiencias"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">{{
                      propsLanguage.header.exp }}</a>
                </li>
                <li class="animate-bottom">
                  <a href="#contatos"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">{{
                      propsLanguage.header.contato }}</a>
                </li>
                <li class="animate-bottom">
                  <div @click="chageTheme()"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">
                    <MoonIcon v-if="darkMode == false" class="text-black w-8 h-8  cursor-pointer" />
                    <SunIcon v-if="darkMode == true" class="text-pink-500 w-8 h-8  cursor-pointer" />
                  </div>
                </li>
                <li class="animate-bottom">
                  <div @click="chageLanguage()"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 dark:text-gray-400 text-2xl lg:dark:hover:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent' : 'block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 lg:border-0 lg:p-0 lg:hover:bg-transparent hover:bg-gray-50 hover:text-blue-700 text-2xl'">
                    <p v-if="language == true" class="cursor-pointer">EN</p>
                    <p v-else class="cursor-pointer">POR</p>
                  </div>
                </li>
              </ul>
            </div>
            <div class="flex sm:hidden">
              <div class="animate-bottom">
                  <div @click="chageTheme()"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3  lg:border-0 lg:p-0 text-gray-400 text-2xl lg:hover:text-white border-gray-700' : 'block py-2 pr-4 pl-3  lg:border-0 lg:p-0 text-2xl text-pink-600'">
                    <MoonIcon v-if="darkMode == false" class="text-pink-600 w-8 h-8  cursor-pointer" />
                    <SunIcon v-if="darkMode == true" class="text-pink-500 w-8 h-8  cursor-pointer" />
                  </div>
                </div>
                <div class="animate-bottom">
                  <div @click="chageLanguage()"
                    :class="darkMode == true ? 'block py-2 pr-4 pl-3  lg:border-0 lg:p-0 text-pink-500 text-2xl  dark:border-gray-700 ' : 'block py-2 pr-4 pl-3  lg:border-0 lg:p-0 text-2xl text-pink-600 font-semibold'">
                    <p v-if="language == true" class="cursor-pointer">EN</p>
                    <p v-else class="cursor-pointer">POR</p>
                  </div>
                </div>
            </div>
          </div>
        </nav>
      </header>
    </div>
    <main class="scroll-container">
      <Sobre class="scroll-page" :darkMode="darkMode" id="main" :propsLanguage=propsLanguage />
      <About class="scroll-page" :darkMode="darkMode" id="sobre" :propsLanguage=propsLanguage />
      <Experiencias class="scroll-page" :darkMode="darkMode" id="experiencias" :propsLanguage=propsLanguage />
      <Contato class="scroll-page" :darkMode="darkMode" id="contatos" :propsLanguage=propsLanguage />
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
  from {
    right: -50px;
    opacity: 0
  }

  to {
    right: 0px;
    opacity: 1
  }
}

@keyframes animatebottom {
  from {
    right: -50px;
    opacity: 0
  }

  to {
    right: 0;
    opacity: 1
  }
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




