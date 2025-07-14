<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

import 'vue3-carousel/dist/carousel.css'
import { Carousel, Navigation, Slide } from 'vue3-carousel';

const images = Array.from({ length: 10 }, (_, index) => ({
  id: index + 1,
  url: `https://picsum.photos/seed/${Math.random()}/800/600`,
}))

const config = {
  height: 200,
  itemsToShow: 2,
  gap: 5,
  wrapAround: true,
}
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <Carousel v-bind="config">
            <Slide v-for="image in images" :key="image.id">
                <img :src="image.url" alt="image" />
            </Slide>

            <template #addons>
            <Navigation />
            </template>
        </Carousel>

        <div class="relative -mt-[200px]">
            <div class="flex m-4 z-10 relative">
                <div class="bg-white mx-2 p-2 text-md w-full text-center">
                    You are on amazon-clone. You can also shop on Amazon.com.<span>Click here</span>
                </div>
            </div>
            <div class="grid grid-cols-3 m-4 z-10 relative">
                <div class="p-1.5 flex">
                    <div class="bg-white p-5">
                        <div class="text-2xl flex font-extrabold">Computers</div>
                        <div class="flex">
                            <img class="object-fill" src="https://dummyimage.com/1097x756/000/fff" alt="computer">
                        </div>
                        <div class="pt-3 -mb-2 text-teal-800 font-bold hover:underline hover:text-req-400 cursor-pointer">
                            Shop Now
                        </div>    
                    </div>
                </div>
                <div class="p-1.5 flex">
                    <div class="bg-white p-5">
                        <div class="text-2xl flex font-extrabold">Computers</div>
                        <div class="flex">
                            <img class="object-fill" src="https://dummyimage.com/1097x756/000/fff" alt="computer">
                        </div>
                        <div class="pt-3 -mb-2 text-teal-800 font-bold hover:underline hover:text-req-400 cursor-pointer">
                            Shop Now
                        </div>    
                    </div>
                </div>
                <div class="p-1.5 flex">
                    <div class="bg-white p-5">
                        <div class="text-2xl flex font-extrabold">Computers</div>
                        <div class="flex">
                            <img class="object-fill" src="https://dummyimage.com/1097x756/000/fff" alt="computer">
                        </div>
                        <div class="pt-3 -mb-2 text-teal-800 font-bold hover:underline hover:text-req-400 cursor-pointer">
                            Shop Now
                        </div>    
                    </div>
                </div>
            </div>
        </div>    
    </AuthenticatedLayout>
</template>

<style>
   .carousel {
    --vc-nav-background: rgba(255, 255, 255, 0.7);
    --vc-nav-border-radius: 100%;
    }

    img {
        border-radius: 8px;
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
</style>
