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
     methods:{
      cangeSelectOption(){
        axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?num=1000&offset=0`, {
          params:{
            archetype: this.store.archetypeSelected || null
          }
        })
        .then( res => {
          this.store.cardsArray = res.data.data
          this.store.numberRequest = res.data.data.length
        })
        .catch(error => {
          this.store.cardsArray = []
        });
      }
    },
    created(){
      this.cangeSelectOption()

      axios.get(`https://db.ygoprodeck.com/api/v7/archetypes.php`)
        .then( res => {
          this.store.archetypeArray = res.data
        });

      
    },
   
    components:{
      HeaderComponet,
      MainComponet,
    }
  }
</script>

<template>
  <HeaderComponet/>
  <MainComponet @selected="cangeSelectOption()"/>
</template>

<style lang="scss">
@use "./assets/scss/main.scss" as *;
</style>
