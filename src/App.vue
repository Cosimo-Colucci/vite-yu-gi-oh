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

    }
}
</script>

<template>

    <HeaderApp/>
    <MainApp/>

</template>

<style lang="scss">
    @import 'bootstrap/scss/bootstrap';
    @import './styles/general.scss';
</style>
