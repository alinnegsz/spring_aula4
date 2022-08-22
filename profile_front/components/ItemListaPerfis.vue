<template>
    <div class="item-perfis mb-2 pt-3 pb-3">
        <b-row>
            <b-col cols="2" class="d-flex align-items-center justify-content-center">
                <b-avatar class="img" v-bind:src=img></b-avatar>
            </b-col>
            <b-col cols="10" class="link d-flex align-items-center justify-content-center">
                <NuxtLink :to="`/${idPerfil}}`">{{perfil}}</NuxtLink>
            </b-col>          
        </b-row>
    </div>
</template>

<script>
   export default {
    name: 'PerfilPage',
    props: ["idPerfil","perfil", "img"]
   }
</script>

<style>
    .item-perfis{
        background-color: rgb(237, 224, 253);
        border: solid rgb(203, 173, 212) 3px;
        border-radius: 10px;
    }
    .img{
        width: 70px;
        height: 70px;
    }
    .link{
        font-size: 20px;
        font-weight: bold; 
    }
</style>
