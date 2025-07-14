<script setup>
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3';
import MapMarkerOutlineIcon from 'vue-material-design-icons/MapMarkerOutline.vue';
import MenuDownIcon from 'vue-material-design-icons/MenuDown.vue'
import MenuIcon from 'vue-material-design-icons/Menu.vue';
import MagnifyIcon from 'vue-material-design-icons/Magnify.vue'
import CartMinusIcon from 'vue-material-design-icons/CartMinus.vue'
import AccountCircleIcon from 'vue-material-design-icons/AccountCircle.vue';
import CloseIcon from 'vue-material-design-icons/Close.vue';
import ChevronRightIcon from 'vue-material-design-icons/ChevronRight.vue';
import { size } from 'lodash';

let showMenu = ref(false);
</script>

<template>
    <div class="main-w-[1150px] bg-gray-100 h-full">
        <div class="flex items-center bg-gray-900 h-[60px] py-2 fixed z-50 min-w-[1150px] w-full">
            <div class="flex">
                <Link class="text-white h-[50px] p-2 pt-3 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer" href="">
                    AMAZON
                </Link>
            </div>   
            <div class="text-white h-[50px] p-2 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
                <div class="flex items-center justify-center">
                    <MapMarkerOutlineIcon class="pt-2 -ml-1" fillColor="#F5F5F5"></MapMarkerOutlineIcon>
                    <div>
                        <div class="text-[13px] text-gray-300 font-extrabold">
                            <div>Delivery to John</div>
                        </div>
                        <div class="text-[15px] text-white -mt-1.5 font-extrabold">
                            <div>London SW2 SW2</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="flex grow items-center h-[45px] px-1">
                <div class="flex items-center justify-center bg-gray-100 border-r border-r-gray-300 font-extrabold text-[11px] text-gray-60 w-[60px] h-[40px] rounded-l-md cursor-pointer">
                    <div class="pt-[3px]">
                        All
                    </div>
                    <MenuDownIcon fillColor="#5e5e5e" :size="20" class="-mr-2"/>
                </div>
                <input class="block w-full border-none border-transparent focus:border-transparent focus:ring-0" type="text">
                <div class="cursor-pointer bg-orange-300 p-[5px] px-2 rounded-r-md">
                    <MagnifyIcon :size="30" />
                </div>
            </div>
            <div class="flex">
                <div class="h-[50px] p-2 pt-3 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray">
                    <div class="flex items-center justify-center mt-2.5 px-1">
                        <img src="https://dummyimage.com/35x20/000/fff" alt="">
                        <div class="text-[15px] text-white -mt-2 -mr-0.5 font-extrabold">EN</div>
                        <MenuDownIcon fillColor="#c2c2c2" :size="20" class="-mr-4 -mt-1.5 pr-1"></MenuDownIcon>
                    </div>
                </div>
                <div class="h-[50px] p-2 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray">
                    <div class="flex items-center justify-center">
                        <div>
                            <div class="text-[12px] text-white font-extrabold">
                                Hello, <span>Sign in</span>
                            </div>
                            <div class="flex items-center">
                                <div class="text-[15px] text-white -mt-2 -mr-0.5 font-extrabold">Account & List</div>
                                <MenuDownIcon fillColor="#c2c2c2" :size="20" class="-mr-4 -mt-1.5 pr-1"></MenuDownIcon>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="h-[50px] p-2 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray">
                    <div class="flex items-center justify-center">
                        <div>
                            <div class="text-[12px] text-white font-extrabold">
                                Returns
                            </div>
                            <div class="flex items-center">
                                <div class="text-[15px] text-white -mt-2 -mr-0.5 font-extrabold">Orders</div>
                            </div>    
                        </div>
                    </div>
                </div>
                <div class="relative h-[50px] p-2 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray">
                    <span class="absolute text-center right-[21px] w-[14px] -top-0 rounded-full text-[20px]">
                        <div class="text-orange-400 font-extrabold bg-gray-900 h-[16px]">0</div>
                    </span>
                    <div class="flex items-center justify-center">
                        <CartMinusIcon fillColor="#FCFCFC" :size="40" class="-mt-0.5" />
                    </div>
                </div>
            </div>
        </div>

        <div class="flex items-center justify-between bg-[#242f3e] h-[38px] fixed z-40 min-w-[1150px] w-full mt-[60px]">
            <div class="flex">
                <div @click="showMenu = true" class="flex h-[30px] border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
                    <div class="flex items-center justify-center px-2">
                        <MenuIcon fillColor="#f5f5f5" :size="26" class="mr-0.5"></MenuIcon>
                        <div class="text-white text-[14px] font-extrabold">
                            All
                        </div>    
                    </div>
                </div>
                <div class="flex h-[30px] border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
                    <div class="flex items-center justify-center px-2">
                        <div class="text-white text-[14px] font-extrabold">
                            Today's Deals
                        </div>    
                    </div>
                </div>
                <div class="flex h-[30px] border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
                    <div class="flex items-center justify-center px-2">
                        <div class="text-white text-[14px] font-extrabold">
                            Gift Cards
                        </div>    
                    </div>
                </div>
                <div class="flex h-[30px] border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
                    <div class="flex items-center justify-center px-2">
                        <div class="text-white text-[14px] font-extrabold">
                            Today's Deals
                        </div>    
                    </div>
                </div>
                <div class="flex h-[30px] border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
                    <div class="flex items-center justify-center px-2">
                        <div class="text-white text-[14px] font-extrabold">
                            Gift Cards
                        </div>    
                    </div>
                </div>
            </div>
            <div class="flex">
                 <div class="flex h-[30px] border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
                    <div class="flex items-center justify-center px-2">
                        <div class="text-white text-[14px] font-extrabold">
                            Holiday Flash Sale
                        </div>    
                    </div>
                </div>
            </div>
        </div>

        <main class="max-w-[1500px] mx-auto pt-[110px]">
            <slot />
        </main>

        <div class="w-full bg-white mt-10">
            <div class="max-w-[1500px] mx-auto">
                <div class="text-[23px] pt-4 font-extrabold">Recommended based on your shopping trends</div>
                <div class="flex justify-center items-stretch">
                    <div class="p-4 text-center mx-auto">
                        <div class="w-[158px] h-[150px] overflow-hidden">
                            <img src="https://via.placeholder.com/158x150" alt="">
                        </div>
                        <div class="w-[160px] text-[12px] py-2 text-teal-600 font-extrabold hover:text-red-600 cursor-pointer">
                            This is a test title
                        </div>
                        <div class="flex justify-start">
                            <div class="text-xs font-extrabold text-red-600 w-full text-left">$99.99</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <footer class="bg-[#232F3E]">
            <div class="bg-[#3747a5] hover:bg-gray-600 w-full p-3.5 cursor-pointer text-white font-extrabold text-center">Back to top</div>
            <div class="flex items-stretch justify-between max-w-[1000px] mx-auto p-10 text-white">
                <ul>
                    <li class="font-extrabold text-lg">Get to now us</li>
                    <li class="hocer:unerline cursor-pointer">Careers</li>
                    <li class="hocer:unerline cursor-pointer">About AWS</li>
                    <li class="hocer:unerline cursor-pointer">Relations</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Devides</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Science</li>
                </ul>
                <ul>
                    <li class="font-extrabold text-lg">Get to now us</li>
                    <li class="hocer:unerline cursor-pointer">Careers</li>
                    <li class="hocer:unerline cursor-pointer">About AWS</li>
                    <li class="hocer:unerline cursor-pointer">Relations</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Devides</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Science</li>
                </ul>
                <ul>
                    <li class="font-extrabold text-lg">Get to now us</li>
                    <li class="hocer:unerline cursor-pointer">Careers</li>
                    <li class="hocer:unerline cursor-pointer">About AWS</li>
                    <li class="hocer:unerline cursor-pointer">Relations</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Devides</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Science</li>
                </ul>
                <ul>
                    <li class="font-extrabold text-lg">Get to now us</li>
                    <li class="hocer:unerline cursor-pointer">Careers</li>
                    <li class="hocer:unerline cursor-pointer">About AWS</li>
                    <li class="hocer:unerline cursor-pointer">Relations</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Devides</li>
                    <li class="hocer:unerline cursor-pointer">Amazon Science</li>
                </ul>
            </div>
        </footer>

        <div v-if="showMenu" class="top-0 z-50 fixed w-full h-full bg-black bg-opacity-70" 
            :class="[showMenu ? 'animate__animated animate__fadeIn animate__faster' : '']"
        >
            <CloseIcon 
                @click="showMenu = false" 
                :size="30" 
                fillColor="#DCDCDC" 
                class="ml-2.5 mt-3.5 left-80 cursor-pointer fixed z-50" 
                :class="[showMenu ? 'animate__animated animate__fadeIn animate__faster' : '']" 
            /> 
            <div class="w-80 h-full bg-white"
                :class="[showMenu ? 'animate__animated animate__slideInLeft animate__faster' : '']"
            >
                <div class="bg-[#232f3e] font-extrabold text-[18px] flex items-center p-2 text-white pl-7">
                    <span>Hello, sign in </span>
                </div>
                <div class="font-extrabold text-[16px] pt-3 pb-1 pl-6 pr-3 text-black">
                    Shop by department
                </div> 
                <div class="hover:bg-gray-200 pl-6 pr-3">
                    <div class="py-2.5 text-[13px] text-black flex justify-between items-center hover:bg-gray-200 cursor-pointer">
                        Computers
                    </div>                
                </div>
            </div>
        </div>
    </div>
</template>
