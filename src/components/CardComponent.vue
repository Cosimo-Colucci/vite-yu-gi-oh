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
    <div>
        <img :src="image" class="" :alt="name + ' image'">
        <div class="">
            <h5 class="">
                {{ name }}
            </h5>
            <p class="">
                {{ type }}
            </p>
        </div>
    </div>
</template>

<style>
</style>