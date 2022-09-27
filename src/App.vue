<template>
  <div id="app">
    <HeaderComponent />
    <MainComponent />
  </div>
</template>

<script>
  import HeaderComponent from '@/components/HeaderComponent.vue'
  import MainComponent from '@/components/MainComponent.vue'
  
  
  export default {
    name: 'App',
    components:{
      HeaderComponent,
      MainComponent
    }
  }
  </script>
  
  <style lang="scss">

    @import './assets/styles/font.scss';

   #app{
    font-family: 'Rubik', sans-serif;
   }
 
    *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Rubik', sans-serif;
    }
  
  body{
    background-color: #1e2d3b;
  }
  
  
  </style>
