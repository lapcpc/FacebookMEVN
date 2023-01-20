<template>
    
    <div class=" bg-gray-200/50 h-full">
     <header class='w-full '>
      <Top />
     </header>
     <main class='  grid grid-cols-11 md:grid-cols-12 '>
      <Sidebar :name="name" /> 
      <Feed />
      <Widgets />
     
          
     </main>
    </div>
</template>
  <script>
 
  import axios from 'axios';
  import Top from '../components/Top.vue' 
  import Feed from '../components/Feed.vue';
  import Sidebar from '../components/Sidebar.vue';
  import Widgets from '../components/Widgets.vue';
  export default {
  components: { Top, Sidebar, Feed, Widgets},
    name: 'Landing',

    data() {
      return {
        name: '',
        email: '',
      }
    },
    created() {
      //user is not authorized
      if (localStorage.getItem('token') === null) {
        this.$router.push('/login');
      }
    },
    mounted() {
      axios.get('https://facebook-mevn.vercel.app/api/user', { headers: { token: localStorage.getItem('token')}})
        .then(res => {
          this.name = res.data.user.name;
          this.email = res.data.user.email;
        })
    },
    methods: {
      logout() {
        localStorage.clear();
        this.$router.push('/login');
      }
    }
  }
  </script>
  