<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import CardComponent from './components/CardComponent.vue';

export default {
    name: 'App',
    data(){
        return{

        }
    },
    components: {
        HeaderApp,
        MainApp,
        CardComponent,

    }
}
</script>

<template>

    <HeaderApp/>
    <MainApp/>
    <CardComponent/>

</template>

<style lang="scss">
    @import './styles/general.scss';
</style>
