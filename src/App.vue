<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';

const users= ref([
  {
    name: "Cristina Sanchez",
    mensaje1: "Como estas?",
    mensaje2: "Cuanto vale?",
    mensaje3: "Empanadas a 20.000"
  },
  {
    name: "Paola Alverado",
    mensaje1: "Como estas Uwu?",
    mensaje2: "Cuanto vale?",
    mensaje3: "Empanadas a 20.000"
  },
  {
    name: "Violet Sanchez",
    mensaje1: "Como estas Popi?",
    mensaje2: "Cuanto vale?",
    mensaje3: "Empanadas a 20.000"
  }

])

let user= ref(users.value[0]);

const mostrar= function(userp){
  user.value= userp;
}
</script>

<template>
<div class="flex h-screen">
  <div class="bg-slate-800 w-[150px]">
    <img src="https://i.pinimg.com/550x/8d/e7/fa/8de7fa2af12330350613ede63532c4fb.jpg" alt="" class="w-24 rounded-lg ml-6 mt-6">
    <p class="ml-6 text-gray-400">Perfil</p>
  </div>
  <div class="bg-slate-700 w-[700px]">
    <h1 class="text-4xl ml-8 mt-8 font-semibold text-white">TENDENCIAS</h1>
    <p class="ml-8 mt-8 text-gray-400 text-xl">#Titanic</p>
    <p class="ml-8 mt-4 text-gray-400 text-xl">#Millonarios</p>
    <p class="ml-8 mt-4 text-gray-400 text-xl">#FinalSemestre :D</p>
    <p class="ml-8 mt-4 text-gray-400 text-xl">#UFC</p>
    <p class="ml-8 mt-4 text-gray-400 text-xl">#ColombiaMarcha</p>
    <p class="ml-8 mt-4 text-gray-400 text-xl">#UFPSO</p>
    <h1 class="ml-8 mt-[250px] text-4xl text-white font-semibold">MENSAJES DIRECTOS</h1>
    <div class="flex bg-slate-600 mx-8 mt-5 h-[100px] rounded-lg cursor-pointer" @click="mostrar(users[0])">
      <img src="https://i.pinimg.com/550x/8d/e7/fa/8de7fa2af12330350613ede63532c4fb.jpg" alt="" class="w-18 rounded-full mt-3 mb-3 ml-5">
      <div>
        <p class="ml-3 text-xl mt-6 text-white font-semibold">Cristina Sanchez</p>
        <p class="text-md ml-3 text-gray-400">Hace 10 minutos</p>
      </div>
    </div>
    <div class="flex bg-slate-600 mx-8 mt-5 h-[100px] rounded-lg cursor-pointer" @click="mostrar(users[1])">
      <img src="https://i.pinimg.com/550x/8d/e7/fa/8de7fa2af12330350613ede63532c4fb.jpg" alt="" class="w-18 rounded-full mt-3 mb-3 ml-5">
      <div>
        <p class="ml-3 text-xl mt-6 text-white font-semibold">Paola Alverado</p>
        <p class="text-md ml-3 text-gray-400">Hace 10 minutos</p>
      </div>
    </div>
    <div class="flex bg-slate-600 mx-8 mt-5 h-[100px] rounded-lg cursor-pointer" @click="mostrar(users[2])">
      <img src="https://i.pinimg.com/550x/8d/e7/fa/8de7fa2af12330350613ede63532c4fb.jpg" alt="" class="w-18 rounded-full mt-3 mb-3 ml-5">
      <div>
        <p class="ml-3 text-xl mt-6 text-white font-semibold">Violet Sanchez</p>
        <p class="text-md ml-3 text-gray-400">Hace 10 minutos</p>
      </div>
    </div>
  </div>
  <div class="bg-slate-600 w-[800px]">
    <HelloWorld :user="user"/>
  </div>
  <div class="bg-slate-800 w-[525px]">
    <h1 class="text-4xl ml-8 mt-8 font-semibold text-white">PUBLICIDAD</h1>
    <img src="https://img.freepik.com/psd-gratis/promocion-redes-sociales-alimentos-plantilla-diseno-publicacion-banner-instagram_202595-285.jpg?w=2000" alt="" class="w-[400px] ml-16 mt-8 rounded-xl">
    <img src="https://img.freepik.com/psd-gratis/promocion-redes-sociales-alimentos-plantilla-diseno-publicacion-banner-instagram_202595-285.jpg?w=2000" alt="" class="w-[400px] ml-16 mt-8 rounded-xl">
  </div>
</div>
</template>


