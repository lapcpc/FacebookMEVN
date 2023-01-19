<template>
        <div class='bg-white rounded-lg shadow-md'>
        <div class='flex flex-row  justify-center '>
            <div :class="{'border-b-4 border-b-blue-500':top == 1 , '': top != 1}" class="cursor-pointer w-[30%]"  @click.prevent="setTop(1)" >
                <Subtitle  title="Historias" ><BookOpenIcon class="text-blue-500 w-5 h-5 mt-0.5"/> </Subtitle>
            </div>
            <div :class="{'border-b-4 border-b-blue-500':top == 2 , '': top != 2}" class="cursor-pointer w-[30%]"  @click.prevent="setTop(2)" >
                <Subtitle title="Reels" ><VideoCameraIcon class="text-blue-500 w-5 h-5 mt-0.5"/></Subtitle>
            </div>
            <div :class="{'border-b-4 border-b-blue-500':top == 3 , '': top != 3}" class="cursor-pointer w-[30%]"  @click.prevent="setTop(3)" >
                <Subtitle title="Salas" ><PlayCircleIcon  class="text-blue-500 w-5 h-5 mt-0.5"/></Subtitle>
            </div>
        </div>
        <div class=' flex flex-row m-2 ' id='slider'>
           <!-- Sliders -->
            <div 
            class='cursor-pointer bg-white p-1 rounded-full shadow-md w-fit h-fit absolute top-[10%] lg:top-[20%] '
            :click="slideLeft()"
            >
                <ChevronLeftIcon class='h-6 w-6' />
            </div>
            <div  
            class='cursor-pointer bg-white p-1 rounded-full shadow-md w-fit h-fit absolute top-[10%] lg:top-[20%] left-[90%] lg:left-[60%] sm:left-[80%] z-50'
             :click="slideRight()"
            >
                <ChevronRightIcon  :click="slideRight()" class='h-6 w-6' />
            </div>
            <!-- Crear historias -->
                <div class=' flex-none bg-white shadow-lg rounded-md w-28 h-48 m-2 '>
                    <img class=' object-cover w-40 h-36 rounded-md' src="https://pbs.twimg.com/profile_images/1561604184289558529/Bq62M5zI_400x400.jpg" />
                    <div class='  h-full'>
                        <div class='bg-blue-500 p-1 border-4 border-white w-fit h-fit relative rounded-full   z-50 -top-5 left-[35%]'>
                        <PlusIcon class='  text-white  w-5 h-5' />
                        </div>
                    
                        <p class=' relative text-xs text-center -top-3 font-semibold '>Crear historia</p>
                    </div>
                </div>
            <!-- Historiias -->
                <div class=' flex flex-row'>
                 
                    <div v-for="img in imgs" :key="img" class='  bg-white shadow-lg rounded-md w-28 h-48 m-2'>
                        <img class='z-10 object-cover w-52 h-48 rounded-md' src="https://i.pinimg.com/736x/7c/0c/c9/7c0cc97b855fe411e11b30ea9809cba3.jpg" />
                        <p class='text-white text-sm ml-2 z-20 -top-6 relative'> Luis Pinot</p>    
                        <img class='relative rounded-full -top-[107%] border-2 border-blue-700 ml-1 z-20 object-cover w-10 h-10 ' src="https://pbs.twimg.com/profile_images/1561604184289558529/Bq62M5zI_400x400.jpg" />
                    </div>
                  
                </div>
        </div>
        
        
    </div>
</template>
<script>
import { PlusIcon, ChevronRightIcon, ChevronLeftIcon, BookOpenIcon, VideoCameraIcon, PlayCircleIcon} from '@heroicons/vue/24/solid';
import Subtitle from './Subtitle.vue';
export default {
   components:{
    PlusIcon,
    Subtitle,
    ChevronRightIcon,
    ChevronLeftIcon,
    BookOpenIcon, VideoCameraIcon, PlayCircleIcon
   },
    data() {
      return {
        top: 1 ,
        imgs : [1,2,3,4,5,6,7]
    }},
    methods:{
        setTop(n){
            this.top = n
        },
        slideRight(){},
        slideLeft(){}
    }
}
</script>
<style >
#slider {
    scroll-behavior: smooth;
    scrollbar-width: none;
    overflow-x: scroll;
    overflow-y: hidden;
    
  }
#slider::-webkit-scrollbar {
    display: none;
}
</style>