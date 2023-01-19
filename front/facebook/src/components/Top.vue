
<template>
 <div class='grid grid-cols-12 w-full justify-between bg-white shadow-md'>
        <div class=' p-2 mt-2 ml-2 col-span-2 '>
            <img class=' h-[21px] ' src="https://logodownload.org/wp-content/uploads/2014/09/facebook-logo-15.png"/>
        </div>
        <div class='w-fit sm:w-7/12 sm:h-3/4 mx-auto col-span-7 flex flex-row my-auto rounded-full p-2 sm:p-0 sm:px-5  bg-gray-200'>
            <MagnifyingGlassIcon class='w-5 h-5 sm:mt-2'/>
            <input class='hidden sm:inline bg-gray-200' placeholder='' />
    
        </div>
        <div class=' mr-5 mt-1 space-x-1 col-span-3 flex flex-row justify-end '>
           <div class='p-2 rounded-full bg-gray-200 w-fit h-fit'>
                <ChatBubbleLeftEllipsisIcon class='w-6 h-6'/>
           </div>
           <div class='p-2 rounded-full bg-gray-200 w-fit h-fit'>
                <BellIcon class='w-6 h-6' />
           </div>
           <div @click.prevent="logout()" class='p-2 rounded-full bg-gray-200 w-fit h-fit cursor-pointer'>
                <ArrowRightOnRectangleIcon class='w-6 h-6' />
           </div>
            

        </div>
    </div>
</template>

<script>
import { MagnifyingGlassIcon, ChatBubbleLeftEllipsisIcon, BellIcon, ArrowRightOnRectangleIcon } from '@heroicons/vue/24/solid'

export default {
  components: {  MagnifyingGlassIcon, ChatBubbleLeftEllipsisIcon, BellIcon,ArrowRightOnRectangleIcon },
  methods:{
    logout() {
        localStorage.clear();
        this.$router.push('/login');
      }
  }
}
</script>