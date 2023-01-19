<template>
    <div class="alert-box " :class="{hidden:this.estado == false}">
    <div class="flex flex-row justify-between">
        <strong>Great!</strong>
        <XMarkIcon class="w-6 h-6 text-black cursor-pointer" @click.prevent="cerrar()" />
    </div>
      <br/>
      <slot></slot>
    </div>
  </template>
  <script>
  import { XMarkIcon } from '@heroicons/vue/24/solid';
  export default {
    props: ['close', 'estado'],
    components:{
        XMarkIcon
    },
    methods:{
        cerrar(){
            this.close()
        }
    }
  }
  </script>
  
  <style scoped>
  .alert-box {
    color: #666;
    border: 1px solid green;
    border-radius: 4px;
    padding: 20px;
    background-color: #f8f8f8;
  }
    
  strong {
      color: green;    
  }
  </style>