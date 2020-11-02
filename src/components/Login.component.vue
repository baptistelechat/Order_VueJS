<template>
  <div id="login">
        <div class="row">
            <div class="jumbotron head">
                                
                <div class="form-group">
                    <label for="login">Nom d'utilisateur</label>
                    <input type="text" name="login" id="username" class="form-control" placeholder="Saisir votre nom d'utilisateur" aria-describedby="helpId" v-model="username">
                    <small id="helpId" class="text-muted">Trouver un nom original 😄</small>
                </div>

                <p>Vous êtes connecté en tant que <strong>{{ username }}</strong></p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Login',
        props: {
            username: String
        }
    }
</script>

<style>
.jumbotron {
    margin-top: 32px;
}
.head {
    margin-left: auto;
    margin-right: auto;
    width: 450px;
}
</style>
