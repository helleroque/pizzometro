<template>

<div class="">
        <img alt="" src="../assets/pizzza.png" height="300"/>
      </div>
      <!-- fim da imagem -->

    <main class=" w-100">
        <div class="container col-3 text-center mt-4">
            <div class="input-group mb-3">
                <label class="form-control">Adultos</label>
                <input type="text" class="form-control" v-model='pessoas["adulto"]["quantidade"]'>
            </div>
        
            <div class="input-group mb-3 col-6">
                <label class="form-control">Crianças </label>
                <input type="text" class="form-control" v-model='pessoas["crianca"]["quantidade"]'>
            </div>
    
            <button type="button" v-on:click="calcularPizza()">Calcular</button><br><br>
    
        </div>
    
        <Resultado 
            v-bind:PizzaG="pizzas.PizzaG.quantidade"
            v-bind:PizzaP="pizzas.PizzaP.quantidade" 
            v-bind:total="total"
            class="p-5"
        ></Resultado>
    </main>
    
 
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">
</template>

<script>
import Resultado from './Resultado.vue'

    export default {
    name: "Valores",
    data() {
        return {
            total: 0,
            pessoas: {
                crianca: {
                    quantidade: 0,
                    come: 2
                },
                adulto: {
                    quantidade: 0,
                    come: 3
                }
            },
            pizzas: {
                PizzaG: {
                    pedacos: 12,
                    quantidade: 0
                },
                PizzaP: {
                    pedacos: 8,
                    quantidade: 0
                }
            }
        };
    },
    methods: {
        calcularPizza() {
            this.total = (this.pessoas["crianca"]["come"] * this.pessoas["crianca"]["quantidade"]) + (this.pessoas["adulto"]["come"] * this.pessoas["adulto"]["quantidade"]);
            let sobra = this.total;
            for (const prop in this.pizzas) {
                let qnt = parseInt(sobra / this.pizzas[prop]["pedacos"]);
                this.pizzas[prop]["quantidade"] = qnt;
                sobra -= qnt * this.pizzas[prop]["pedacos"];
                if (this.pizzas[prop]["pedacos"] == 8 && sobra <= 7 && sobra > 0) {
                    this.pizzas[prop]["quantidade"]++;
                }
            }
        }
    },
    components: { Resultado}
}

</script>

<style>

</style>