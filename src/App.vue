<script>
  import HeaderComponet from './components/HeaderComponets/HeaderComponet.vue';
  import MainComponet from './components/MainComponets/MainComponet.vue';
  import axios from 'axios'

  export default{
    data(){
      return {
        cardsArray:[]
      }
    },
    created(){
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=0')
        .then( res => {
          this.cardsArray = res.data.data
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
  <MainComponet :cardsArray="cardsArray"/>
</template>

<style lang="scss">
@use "./assets/scss/main.scss" as *;
</style>
