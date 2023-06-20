<script>
    export default{
            name: 'CardComponenet',
            data(){
                return{

                }
            },
            props:{
                name : String,
                type : String,
                image : String,
            }
        }
</script>

<template>

<div class="card col-3" style="width: 18rem;">
  <img :src="image" class="card-img-top" :alt="name + ' image'">
  <div class="card-body">
    <h5 class="card-title">{{ name }}</h5>
    <p class="card-text">{{ type }}</p>
  </div>
</div>
    
</template>

<style>
</style>