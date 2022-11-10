<template>
  <!-- CSS -->
  <body>
    <header >
    </header>
  
    <main class="bg-ligth">
      <div class="fundo"></div>
      <h1 class="text-dark m-5">Calcule a quantidade de pessoas e 
        descubra qual tamanho de pizza 
        você deve comprar</h1>
      <Valores></Valores>
    </main>
  
    <footer></footer>
  </body>
    
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">
  </template>
  
  <script>
  
  import Valores from "./components/Valores.vue";
  
    export default {
      name: 'App',
      components:{
        Valores
      }
    }
    
  
  </script>
  
  <style>
  
    main h1{
      font-size: 27px;
    }
    main{
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
    }
  </style>
  