<script>
  import HeaderComponet from './components/HeaderComponets/HeaderComponet.vue';
  import MainComponet from './components/MainComponets/MainComponet.vue';
  import { store } from './store.js';
  import axios from 'axios';

  export default{
    data(){
      return {
        store
      }
    },
    created(){
      axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?num=${this.store.numberRequest}&offset=0`)
        .then( res => {
          this.store.cardsArray = res.data.data
        })
    },
    components:{
      HeaderComponet,
      MainComponet,
    }
  }
</script>

<template>
  <HeaderComponet/>
  <MainComponet/>
</template>

<style lang="scss">
@use "./assets/scss/main.scss" as *;
</style>
