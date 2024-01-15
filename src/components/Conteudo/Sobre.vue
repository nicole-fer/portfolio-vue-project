<script setup>
const props = defineProps({
    darkMode: Boolean,
    propsLanguage: Object,
})

console.log(props.propsLanguage)
</script>

<template>
  <div>
    <div  :class="darkMode == true ? 'grid grid-cols-5  text-white sm:h-screen py-10 sm:py-0 bg-gradient-to-b from-gray-800 to-cyan-800' : 'bg-gradient-to-b from-pink-100 to-pink-200  grid grid-cols-5 sm:h-screen py-10'">
      <div class="sm:px-8	flex place-items-center sm:col-span-3 col-span-5 sm:mr-12 px-4">
          <div class="sm:-mt-32">
              <p  :class=" darkMode==true  ? 'animate-bottom box sm:text-7xl text-4xl font-mono font-medium text-pink-400' : 'box sm:text-7xl text-4xl font-mono font-medium text-pink-600'">{{ propsLanguage.sobre.nome }}</p>
            <p :class="darkMode==true ? 'animate-p sm:text-2xl text-xl text-justify text-pink-200 pr-3 mt-5': 'sm:text-2xl mt-5 text-xl text-justify text-blue-950'"> {{ propsLanguage.sobre.apresentacao }}</p>
          </div>
        </div>
        <div class="sm:-mt-12 place-items-center sm:col-span-2 flex justify-end sm:flex hidden">
            <img class="h-2/3 w-3/5" src="../../assets/img/icon.png"/>
        </div>
    </div>
  </div>
</template>

<style scoped>
.teste{
    background-image: url('../../assets/img/bgDark-image.png');
}

.animate-bottom {
  position: relative;
  -webkit-animation-name: animatebottom;
  -webkit-animation-duration: 1s;
  animation-name: animatebottom;
  animation-duration: 1s
}

@-webkit-keyframes animatebottom {
  from { left:-100px; opacity:0 } 
  to { left:0px; opacity:1 }
}

@keyframes animatebottom { 
  from{ left:-100px; opacity:0 } 
  to{ left:0; opacity:1 }
}

.animate-p {
  position: relative;
  -webkit-animation-name: animatep;
  -webkit-animation-duration: 1s;
  animation-name: animatep;
  animation-duration: 1.5s
}

@-webkit-keyframes animatep {
  from { left:-100px; opacity:0 } 
  to { left:0px; opacity:1 }
}

@keyframes animatep { 
  from{ left:-150px; opacity:0 } 
  to{ left:0; opacity:1 }
}



</style>
