<script setup>
 import {fullImage, images, changeImage} from './data/carousel.js';
</script>



<template>
   <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Events & Reactivity</h1>
        <div class="">
            <!-- <CCarousel controls indicators transition="crossfade">
              <CCarouselItem>
                <img @click="changeImage(image)" class="cursor-pointer" v-for="image in images" :key="image.thumb" :src="image.thumb">
              </CCarouselItem>
            </CCarousel> -->
            <div class="flex space-x-2">
                <img @click="changeImage(image)" class="cursor-pointer" v-for="image in images" :key="image.thumb" :src="image.thumb">
                <!-- <img class="cursor-pointer" src="https://images.unsplash.com/photo-1682695794816-7b9da18ed470?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1yZWxhdGVkfDZ8fHxlbnwwfHx8fHw%3D&auto=format&fit=crop&w=300&q=60" alt="">
                <img class="cursor-pointer" src="https://images.unsplash.com/photo-1682685797661-9e0c87f59c60?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1yZWxhdGVkfDE4fHx8ZW58MHx8fHx8&auto=format&fit=crop&w=300&q=60" alt="">
                <img class="cursor-pointer" src="https://plus.unsplash.com/premium_photo-1666963323736-5ee1c16ef19d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1yZWxhdGVkfDE2fHx8ZW58MHx8fHx8&auto=format&fit=crop&w=300&q=60" alt=""> -->
            </div>
            <div class="mt-10">
                <img class="cursor-pointer w-full" :src="fullImage" alt="">
            </div>
        </div>
    </section>
</template>


<style scoped>

</style>
