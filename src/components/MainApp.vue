<script>
import CardComponent from './CardComponent.vue';
import {store} from '../store'

    export default{
        name: 'MainApp',
        data(){
            return{
                store,
            }
        },
        components: {
            CardComponent,
        }
    }
</script>

<template>
    <div>
        <h2>
            Main
        </h2>
    </div>
</template>

<style lang="scss">
</style>