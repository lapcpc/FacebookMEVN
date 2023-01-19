<template>
    <div class='bg-white rounded-lg shadow-md'>
        <div>
            <div class='flex flex-row space-x-2 m-2 p-2'>
            
                <img src='https://pbs.twimg.com/profile_images/1561604184289558529/Bq62M5zI_400x400.jpg' class='rounded-full w-10 h-10' />
                <input class='w-full rounded-full p-2 placeholder:text-slate-500 bg-gray-100' placeholder='Que estas pensando, Luis Alejandro' />

            </div>
            <hr />
            <div class='flex flex-row justify-between py-3 text-slate-500'>
                <div class='space-x-2 flex flex-row w-fit mx-auto'>
                  <VideoCameraIcon class='text-red-500 h-6 w-6' />
                  <p>Video en vivo</p>
                </div>
                <div class='space-x-2 flex flex-row w-fit mx-auto'>
                  <PhotoIcon class='text-green-500 h-6 w-6' />
                  <p>Foto/video</p>
                </div>
                <div class='space-x-2 flex flex-row w-fit mx-auto'>
                  <FaceSmileIcon class='text-yellow-500 h-6 w-6' />
                  <p>Feeling/Activity</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import {  VideoCameraIcon, PhotoIcon, FaceSmileIcon } from '@heroicons/vue/24/solid';
export default {
    components:{
        VideoCameraIcon, PhotoIcon, FaceSmileIcon
    }
}
</script>