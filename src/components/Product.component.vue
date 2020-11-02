<template>
    <div class="row justify-content-center">
        <div class="col-5-lg col-12-sm">
            <h1>Produits disponible :</h1>
            <div class="row">
                <div class="col-3" v-for="produit in produits" v-bind:key="produit">
                    <h5 class="jumbotron">
                        {{produit}}
                        <br>
                        <br>
                        <button class="btn btn-secondary" v-on:click="commander(produit)">Commander</button>
                    </h5>
                </div>
            </div>
        </div>
        <div class="col-4-lg col-12-sm">
            <h1 v-if="commandes.length>0">Produits commandés :</h1>
            <ul class="list-group">
                <li v-for="commande in commandes" v-bind:key="commande" class="list-group-item">{{commande}}</li>
            </ul>
        </div>
    </div>
    
</template>
    
<script>
    export default {
        name: 'Product',
        data() {
            return {
                produits: ["Pizza","Hamburger","Hot Dog","Tacos"],
                commandes:[]
            }
        },
        methods: {
            commander: function (param) { 
                this.commandes.push(param);
                console.log('📝 Ajout de : '+param);
                console.log('🛒 Commande : '+this.commandes);
            }
        }
    }
</script>

<style>
.list-group-item {
    margin-left: auto;
    margin-right: auto;
    width: 250px;
}
</style>