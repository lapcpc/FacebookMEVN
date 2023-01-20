<template>
    <div @click.prevent="this.accion()" :class="{ hidden:this.estado == true,absolute:this.estado == false}" class="w-screen h-screen bg-opacity-50 bg-gray-500" >
        <div @click.stop="hijo()" class='p-2 shadow-lg rounded-md relative top-[30%] left-[15%] sm:left-[20%] md:left-[25%] lg:left-[35%] w-2/3 sm:w-6/12 md:w-5/12 lg:w-4/12 bg-white '>
           <h1 class='text-center p-2 text-2xl font-semibold'>Create user</h1> 
           <form class='flex flex-col space-y-2 p-2 justify-center'>
           <div class='flex flex-col w-full mx-auto space-y-2'>
                <input  v-model="name" type="text" class='mx-auto w-11/12 rounded-md p-2 outline-none border border-slate-200  focus:border-sky-500  placeholder:' placeholder='Name' />
                <input  v-model="email" type="email" class='mx-auto w-11/12 rounded-md p-2 outline-none border border-slate-200  focus:border-sky-500  placeholder:' placeholder='Email'/>
                <input  v-model="password" type="password" class='mx-auto w-11/12 rounded-md   p-2 outline-none border border-slate-200 focus:border-sky-500  placeholder:' placeholder='Password'/>
           </div>
            <br />
            <button @click.prevent="signup()" class='bg-green-500 w-1/3 mx-auto p-2 rounded-lg font-semibold text-white'>Register Now</button>
           </form>
            {{error}}
        </div>
    </div>
</template>
<script>
import axios from 'axios'

export default{
    props: ['estado','accion', 'accion2'],

    data(){
        return {
        name: '',
        email: '',
        password: '',
        error: '',
      }
    },
    methods:{
        signup(){

        },
        hijo(e){
        },
        signup() {
        let newUser = {
          name: this.name,
          email: this.email,
          password: this.password
        }
        axios.post('https://facebook-mevn.vercel.app/api/signup', newUser)
          .then(res => {
            this.error = '';
            this.accion2();
           // this.$router.push('/login');
        
            
          }, err => {
            console.log(err.response)
            this.error = err.response.data.error
          })
      }
    }
}
</script>
