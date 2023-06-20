<script>
import CardComponent from './CardComponent.vue';

import {store} from '../store.js'
import axios from 'axios';

    export default{
        name: 'MainApp',
        data(){
            return{
                apiUrl:'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
                store,
            }
        },
        components: {
            CardComponent,
        },
        created(){
             axios.get(this.apiUrl)
            .then( (response) => {
                console.log(response);
            })
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