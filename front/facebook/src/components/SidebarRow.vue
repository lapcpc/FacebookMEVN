<template>
     <div className='flex flex-row space-x-3 space-y-0.5  ml-2 p-1 cursor-pointer hover:bg-gray-100 lg:hover:bg-gray-200'>
        
        <slot></slot>
        <p className='hidden lg:inline'> {{ title }}</p>
    </div>
</template>
<script>
export default {
    props:['title']
}
</script>
