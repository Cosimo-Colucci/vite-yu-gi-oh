<script>
import CardComponent from './CardComponent.vue';
import SelectComponent from './SelectComponent.vue';

import {store} from '../store.js'
import axios from 'axios';

    export default{
        name: 'MainApp',
        data(){
            return{
                apiUrl:'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
                store,
                cardComponentList:[]
            }
        },
        props:{
            cardList : Array,
        },
        components: {
            CardComponent,
            SelectComponent,
        },
        created(){
             axios.get(this.apiUrl)
            .then( (response) => {
                console.log(response.data.data);
                this.cardComponentList = response.data.data;
            })
        }
    }
</script>

<template>
        <SelectComponent/>
        <div class="container">
            <div class="row">
                
                <CardComponent v-for="card in cardComponentList"
                    :name="card.name"
                    :type="card.type"
                    :image="card.card_images[0].image_url"
                />

            </div>
        </div>

</template>

<style lang="scss">
</style>