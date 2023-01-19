<template>
 <div class='bg-gray-100/90 flex flex-col lg:flex-row   lg:space-x-10  justify-center h-screen'>
    <RegistroModal :estado="visibilidad" :accion="cambiarEstado" :accion2="usuarioCreado" />
    
    <div class='my-auto mx-auto lg:mx-0 lg:my-0 flex flex-col justify-center '>
    <AlertBox :estado="visibilidad2" :close="cerrarAlerta">
      The user was registered succesfully!
    </AlertBox>
      <div class=' max-w-screen-sm'>
      <img class="w-[50%]" src="https://static.xx.fbcdn.net/rsrc.php/y8/r/dF5SId3UHWd.svg" />
      <p class='ml-3 text-2xl mt-4'>
        Facebook te ayuda a comunicarte y compartir con las personas que forman parte de tu vida.
      </p>
      </div>
     
  </div>
  <div class='mx-auto border border-slate-200 w-10/12 md:w-7/12 lg:w-[25%] p-2 bg-white my-auto flex flex-row  rounded-lg shadow-xl'>
         
    <div class='w-full '>

            <input 
     
              type="email"
              v-model="email"
              class='focus:outline-none focus:border-blue-500 focus:border rounded-lg focus:shadow-sm focus:shadow-blue-500/50  w-11/12 placeholder:min-w-full m-2 p-2' 
              placeholder='Username' />
            <br/>
            <input
            type="password"
            v-model="password"
            class='focus:outline-none focus:border-blue-500 focus:border rounded-lg focus:shadow-sm focus:shadow-blue-500/50   w-11/12 placeholder:min-w-full m-2 p-2' placeholder='Password' />
            <br/>
            <button @click.prevent="login()" class=' bg-blue-500 hover:bg-blue-500/50 text-white w-11/12 rounded-md text-xl font-medium placeholder:min-w-full m-1 p-2.5'>Sign In</button>
            <p class='text-blue-600 text-center w-11/12 placeholder:min-w-full m-2 p-2'>Forgot password?</p>
            <hr class='mb-3' />
            <div class='flex flex-row'>
              <button @click.prevent="cambiarEstado()" class='text-white bg-green-500 hover:bg-green-500/50 w-6/12 rounded-lg font-bold placeholder:min-w-full mx-auto my-1 p-3'>Create account</button> 
            </div>
          </div>
    </div>
 </div>
</template>
  <script>
  /*
  <div>
      EMAIL: <input type="text" v-model="email"> <br/>
      PASSWORD: <input type="password" v-model="password"> <br/>
      <button @click="login">login</button>
      {{ error }}
    </div>
  */
  import axios from 'axios';
  import RegistroModal from'../components/RegistroModal.vue'
  import AlertBox from '../components/AlertBox.vue'
  export default {
    name: 'Login',
    components:{
      RegistroModal,
      AlertBox
    },
    data() {
      return {
        email: '',
        password: '',
        error: '',
        visibilidad:true,
        visibilidad2: false,
      }
    },
    methods: {
      cambiarEstado(){
        this.visibilidad = !this.visibilidad
      },
      cerrarAlerta(){
        this.visibilidad2 = !this.visibilidad2
      },
      usuarioCreado(){
        this.visibilidad = !this.visibilidad
        this.visibilidad2 = !this.visibilidad2
      
      }
      ,
      login() {
        let user = {
          email: this.email,
          password: this.password
        }
        axios.post('http://localhost:5000/api/login', user)
          .then(res => {
            //if successfull
            if (res.status === 200) {
              localStorage.setItem('token', res.data.token);
              this.$router.push('/');
            }
          }, err => {
            console.log(err.response);
            this.error = err.response.data.error
          })
      },
      

    }
  }
  </script>
 