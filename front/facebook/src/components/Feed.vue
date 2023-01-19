<template>
    <div className='col-span-10 sm:w-10/12 md:w-9/12  w-11/12 relative md:-left-14 lg:-left-0 lg:static md:col-span-9 lg:col-span-7  lg:w-7/12 mx-auto mt-2 bg-gray-100'>
        <TopFeed />
        <CreatePost />
        <Post />
      
    </div>
</template>
<script>
import TopFeed from './TopFeed.vue';
import CreatePost from './CreatePost.vue';
import Post from './Post.vue';
export default {
   components:{
    TopFeed,
    CreatePost,
    Post
   }

}
</script>