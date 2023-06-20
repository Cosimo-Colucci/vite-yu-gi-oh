<script>
    export default{
            name: 'CardComponenet',
            data(){
                return{

                }
            },
            props:{
                name : String,
                species : String,
                status : String,
                image : String,
            }
        }
</script>

<template>
    <div>
        <img :src="image" class="" :alt="name + ' image'">
        <div class="">
            <h5 class="">
                {{ name }}
            </h5>
            <p class="">
                {{ species }} - <small class=""> {{ status }}</small>
            </p>
        </div>
    </div>
</template>

<style>
</style>