<template>
<div class='w-full bg-white my-2 rounded-lg shadow-md'>

         <!--   Header Post  -->
        <div class='flex flex-row  mx-4 pt-4'>
            <div class='w-fit p-1'>
                <img class='w-10 h-10 rounded-full' src="https://pbs.twimg.com/profile_images/1561604184289558529/Bq62M5zI_400x400.jpg" />
            </div>
            <div class='flex flex-row justify-between w-full'>
                <div class='flex flex-col p-2 '> 
                    <p class='text-sm'>Luis Alejandro Pinot Campos</p>
                    <p class=' text-xs'>2h</p>
                </div>
                <div class='flex flex-row space-x-2'>
                    <EllipsisHorizontalIcon class='w-7 h-7' />
                    <XMarkIcon class='w-7 h-7' />
                </div>

            </div>
        </div>
        
        <!--  Texto e imagen  -->
        <div class='flex flex-col'>
            <p class='text-sm mx-4 mb-4'>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sit amet tellus ullamcorper, interdum velit sit amet, rhoncus nisi. Quisque eget hendrerit mauris, in suscipit est. Duis scelerisque mattis tincidunt. Suspendisse a viverra lorem. Donec sit amet facilisis enim, ut dapibus eros. Vestibulum eu interdum erat, eget egestas augue. Praesent id scelerisque neque, ac finibus quam. Pellentesque sit amet imperdiet odio, eget aliquam felis. Suspendisse ac dapibus ante.</p>
            <img class='bg-gray-300 w-full h-[600px] object-contain' src="https://i.pinimg.com/736x/7c/0c/c9/7c0cc97b855fe411e11b30ea9809cba3.jpg" />


        </div>
       <!--   Likes y comentario info  -->
        <div class='py-1 text-xs flex flex-row justify-between mx-2'>
        <div class='flex flex-row space-x-2 mx-3'>
        <FaceSmileIcon class='w-4 h-4 text-yellow-400' />
        <p>5.1 mil</p>
        </div>
        <p>1 vez compartido</p>

        </div>
        <hr/>
        <!--  Me gusta, comentar y compartir  -->
        <div class='text-sm text-slate-500 py-2 flex flex-row justify-between'>
            <div class=' w-fit mx-auto flex flex-row'>
                <HandThumbUpIcon class='w-6 h-6' />
                <p>Me gusta</p>

            </div>
            <div class='w-fit mx-auto flex flex-row'>
                <ChatBubbleBottomCenterIcon class='w-6 h-6' />
                <p>Comentar</p>

            </div>
            <div class='w-fit mx-auto flex flex-row'>
                <ArrowUturnRightIcon class='w-6 h-6' />
                <p>Compartir</p>

            </div>

        </div>
        <!-- Comentar  -->
    </div>
</template>
<script>
import {  ArrowUturnRightIcon, ChatBubbleBottomCenterIcon, FaceSmileIcon, HandThumbUpIcon} from '@heroicons/vue/24/outline';
import {  EllipsisHorizontalIcon, XMarkIcon} from '@heroicons/vue/24/solid';
export default {
    components:{
        ArrowUturnRightIcon, ChatBubbleBottomCenterIcon, FaceSmileIcon, HandThumbUpIcon,EllipsisHorizontalIcon, XMarkIcon
    }
}
</script>