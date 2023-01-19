<template>
     <div className='ml-1 col-span-1 lg:col-span-2 space-y-2 w-3/4 min-w-[45px] text-sm flex flex-col bg-white shadow-md lg:shadow-none lg:bg-transparent '>
            <div className='mt-2'>
                <SidebarRow  title="Home" ><HomeIcon class=" w-5 h-5 text-blue-500" /></SidebarRow>
                <SidebarRow  :title="name" ><UserCircleIcon class=" w-5 h-5 text-black" /></SidebarRow>
            </div>
            
            <hr class='my-2' />
            <SidebarRow  title="Amigos" ><UsersIcon class=" w-5 h-5 text-blue-500" /></SidebarRow>
            <SidebarRow  title="Mas recientes" ><FolderPlusIcon class=" w-5 h-5 text-blue-500" /></SidebarRow>
            <SidebarRow  title="Marketplace" ><BuildingStorefrontIcon class=" w-5 h-5 text-blue-500" /></SidebarRow>
            <SidebarRow  title="Watch" ><PlayCircleIcon class=" w-5 h-5 text-blue-500" /></SidebarRow>
            <SidebarRow  title="Recuerdos" ><ClockIcon class=" w-5 h-5 text-blue-500" /></SidebarRow>
            <SidebarRow  title="Ver todo" ><Squares2X2Icon class=" w-5 h-5 text-blue-500" /></SidebarRow>
    </div>
</template>
<script>
import SidebarRow from './SidebarRow.vue';
import { HomeIcon, UserCircleIcon,UsersIcon, BuildingStorefrontIcon, ClockIcon, PlayCircleIcon, FolderPlusIcon, Squares2X2Icon, UserIcon  } from '@heroicons/vue/24/solid'
export default{
    components:{
        UserCircleIcon,  SidebarRow,HomeIcon, UsersIcon, BuildingStorefrontIcon, ClockIcon, PlayCircleIcon, FolderPlusIcon, Squares2X2Icon, UserIcon
    },
    props:{
        name: String
    }
}
</script>
