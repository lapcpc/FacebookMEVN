<template>
       <div class='py-2 flex flex-row  '>
            <div class=' space-x-1 w-fit flex flex-row mx-auto '>
            <slot></slot>
            <p class=' '>{{title}}</p>
            </div>
        </div>
</template>
<script>
export default {
    props:['title']
}
</script>