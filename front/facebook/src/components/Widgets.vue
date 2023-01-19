<template>
     <div class=' relative md:-left-28 lg:-left-0 hidden md:inline md:col-span-2 md:w-[160%] lg:w-5/6 lg:col-span-3 col-span-3 w-5/6'>
        <!-- Publicidad -->
        <div>
            <p class=' my-3 text-md font-semibold'>Publicidad</p> 
            <div class='space-y-2'>
                <div class='flex flex-row space-x-2'>
                <img class='rounded-md w-28 h-28' src='https://images.pexels.com/photos/1619317/pexels-photo-1619317.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500'/>
                <div class='flex flex-col justify-center'>
                    <p class='text-xs font-semibold'>Elite Software Engineer Wanted</p>   
                    <p class='text-xs'>magia.developer.com</p>   
                    </div>
                </div>
                <div class='flex flex-row space-x-2'>
                <img class='rounded-md w-28 h-28' src='https://blog.unitips.mx/hs-fs/hubfs/Contenido_Informativo_Blog/Universidades%20-%20UNI/UNI-Carreras/08.21_Carreras%20del%20Tec%20de%20Monterrey/TEC_IN.png?width=1200&name=TEC_IN.png' />
                    <div class='flex flex-col justify-center'>
                    <p class='text-xs font-semibold'>Elite Software Engineer Wanted</p>   
                    <p class='text-xs'>magia.developer.com</p>   
                    </div>
                </div>
            </div>
        </div>
       
        <!-- Cumpleaños -->
        <br />
        <div class='flex flex-col w-full '>
        <p class=' my-3 text-md font-semibold'>Cumpleaños</p> 
            <div class='flex flex-row space-x-4 w-full'>
                <img class='w-10 h-10 ' src="https://cdn-icons-png.flaticon.com/512/4067/4067192.png" />
                <p class='text-sm'>
                    Hoy es el cumpleaños de <b>Luis Pinot</b>
                </p>
            </div>

            
        </div>
        <!-- Contactos -->
        <br />
        <div class='flex flex-col '>
            <div class='flex flex-row justify-between'>
                <b class='font-semibold'>Contactos </b>
                <div class='flex flex-row text-slate-500 mt-1.5 space-x-4'>
                    <VideoCameraIcon class='w-4 h-4' />
                    <MagnifyingGlassCircleIcon class='w-4 h-4' />
                    <EllipsisHorizontalCircleIcon class='w-4 h-4' />
                    
                </div>

            </div>
            
            <div class='w-full flex flex-col mt-3 space-y-2'>
               
                    <div v-for="contacto in contactos" :key="contacto" class='space-x-2  flex flex-row w-full hover:bg-gray-200 py-2 px-2 rounded-sm cursor-pointer'>
                        <img src='https://pbs.twimg.com/profile_images/1561604184289558529/Bq62M5zI_400x400.jpg' class='rounded-full w-7 h-7' />
                        <p class='font-semibold text-sm mt-1'>Luis Alejandro Pinot</p>
                    </div>
              
            </div>
        </div>
    </div>
</template>
<script>

import { EllipsisHorizontalCircleIcon, MagnifyingGlassCircleIcon } from '@heroicons/vue/24/outline';
import {VideoCameraIcon} from '@heroicons/vue/24/solid';
export default {
    components:{EllipsisHorizontalCircleIcon, MagnifyingGlassCircleIcon,VideoCameraIcon },

    data(){
        return{
            contactos : [1,2,3,4,5,6,7,8,9,10]
        }
    }
}
</script>