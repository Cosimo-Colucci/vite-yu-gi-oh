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
        props:{
            cardList : Array,
        },
        components: {
            CardComponent,
        },
        created(){
             axios.get(this.apiUrl)
            .then( (response) => {
                console.log(response.data.data);
            })
        }
    }
</script>

<template>
    <div >
        
        <div>
            <CardComponent v-for="card in cardList"
                :name="card.name"
                :type="card.type"
                :image="card.image"
            />
        </div>
    </div>
</template>

<style lang="scss">
</style>