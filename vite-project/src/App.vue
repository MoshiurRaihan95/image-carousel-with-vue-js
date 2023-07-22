<script setup>
 import { data, images, card } from './data/data.js';
 const bgOrange = "bg-orange-400"
 const bgIndigo = "bg-indigo-400"
 const bgGreen = "bg-green-400"
 const textWhite = "text-white text-2xl"
 const textCenter = "flex items-center justify-center"
 const bgRed = "bg-red-600" 
 const bgDrakGreen = "bg-green-600" 


 const weekend = true
</script>



<template>
  <div class="container mx-auto flex items-center justify-center min-h-screen flex-col">
    <h1 class="text-4xl text-black">{{ data.message }}</h1>
    <h1 class="mt-10 text-xl text-gray-700">Today is <span >{{ data.gateCurrentDate() }}</span></h1>
    <h1 class="mt-10 text-2xl text-black-700">You have <span class="bg-slate-400 text-orange-600 p-1 rounded-lg">{{ data.task[6]}}</span> task for today.</h1>
    
    <section class="container mx-auto p-10">
      <h1 class="text-4xl mb-10 text-left">Data Project</h1>
        <section class="main flex space-x-4">
          <div class="flex space-y-4 flex-col w-1/2">
            <img :title="images[0].title" :src="images[0].image" alt="">
            <h2 class="text-xl text-left">{{ images[0].title }}</h2>
            <a target="_blank" :href="images[0].link" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-3 px-4 rounded w-40 text-center">
              Image Source
            </a>
          </div>
        </section>
    </section>
    <section class="container mx-auto">
      <h1 class="text-center text-2xl py-10">Class & Style Binding</h1>

      <section class="flex space-x-10">
        <div class="w-1/3 h-16" :class="[bgOrange,textWhite,textCenter]">Hellllo</div>
        <div class="w-1/3 h-16" :class="bgIndigo"></div>
        <div class="w-1/3 h-16" :class="bgGreen"></div>
      </section>

      <section class="mt-10">
        <div class="h-16 flex items-center justify-center text-white" :class="weekend==true?bgDrakGreen:bgRed">
          It's a weekday!
        </div>
      </section>

      <section class="mt-10 hidden">
        <div class="bg-teal-100 border-t-4 border-teal-500 rounded-b text-teal-900 px-4 py-3 shadow-md" role="alert">
          <p class="font-bold">Our privacy policy has changed</p>
          <p class="text-sm">Make sure you know how these changes affect you.</p>
        </div>
      </section>
    </section>
  </div>
  
</template>


<style scoped>

</style>
