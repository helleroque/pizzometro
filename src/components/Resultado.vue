<template>
    <div class="container col-4">
      <Textos :titulo="msgG" :valor="PizzaG"></Textos>
      <Textos :titulo="msgP" :valor="PizzaP"></Textos>
      <Textos :titulo="msg" :valor="total"></Textos>
    </div>
    

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">
</template>

<script>
import Textos from './Textos.vue';
    export default {
    name: "Valores",
    props: {
        PizzaG: Number,
        PizzaP: Number,
        total: Number
    },
    data(){
      return{
        msgG: "Pizza G",
        msgP: "Pizza P",
        msg: "Total pedaços"
      }
    },
    components: { Textos }
}

    
</script>

<style>

</style>