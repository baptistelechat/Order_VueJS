<template>
    <div class="container">
        <h1>Produits disponible :</h1>
        <div class="row">
            <div class="col-3" v-for="produit in produits" v-bind:key="produit">
                <p class="jumbotron">
                    {{produit}}
                    <br>
                    <button v-on:click="commander">Commander</button>
                </p>
            </div>
        </div>
    </div>
    
</template>
    
<script>
    export default {
        name: 'Product',
        data() {
            return {
                produits: ["Pizza","Hamburger","Hot Dog","Tacos"],
                commande:[]
            }
        },
        methods: {
            commander: function () { 
                console.log("ça marche !!!")
             }
        }
    }
</script>

<style>
.produit {
    color: brown;
}
</style>