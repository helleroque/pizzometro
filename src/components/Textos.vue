<template>
    <div class="input-group mb-3">
        <label class="form-control col-5">{{titulo}}</label>
        <label type="text" class="form-control">{{valor}}</label>
    </div>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">
</template>

<script>
    export default{
        name: "Textos",
        props:{
            titulo: String,
            valor: Number
        }
    }
</script>

<style>


</style>