<template>
    <div class="card-album">
      <img class="w-100" :src="info.poster" :alt="info.title" @error="replaceWrongImageUrl" />
      <h1> {{ info.title }}</h1>
      <div>
        <p>{{ info.author}}</p>
        <p>{{ info.year}}</p>
      </div>
     
    </div>
  </template>
  
  <script>
  
  import errorImage from '@/assets/img/logo.png'
  
  export default {
      name: 'CardComponent',
      props:{
          info: Object
      },
      methods:{
          replaceWrongImageUrl(e){
              console.log('errore');
            e.target.src = errorImage
          }
      }
  }
  </script>
  
  <style lang="scss" scoped>
  .card-album{
      display: flex;
      flex-direction: column;
      padding: 10px;
      background-color: #2e3a46;
      color: #ccc;
      text-align: center;
      height: 100%;
      h1{
        color: white;
        margin-top: 10px;
        
      }
      div{
          color: #7d7772;
          
          margin-top: 20px;
      }
  }
  </style>