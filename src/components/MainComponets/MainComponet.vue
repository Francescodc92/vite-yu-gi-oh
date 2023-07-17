<script>
import ColComponet from './ColComponet.vue';
export default{
  components:{
    ColComponet
  },
  props:{
    cardsArray:{
      type:Array,
      default:[],
    }
  }
}
</script>
<template>
 <main>
  <div class="container">
    <div class="ms-main-top py-3 px-2">
      <select class="form-select " aria-label="Default select example">
        <option selected>Alien</option>
      </select>
    </div>
    <div class="ms-main-bottom h-100 p-4">
      <div class="ms-header-cards">
        <p class="text-white py-3 px-2 mb-1">Found <span>{{ cardsArray.length }}</span> cards</p>
      </div>
      <div class="ms-cards row align-items-stretch justify-content-lg-between row-gap-4">
        <ColComponet :cardsArray="cardsArray"/>
      </div>
    </div>
  </div>
  
 </main>
</template>
<style lang="scss" scoped>
main {
  background-color: #D48F38;
  .form-select{
    max-width: 150px;
  }
  .ms-main-bottom{
    background-color: #fff;
    .ms-header-cards{
      background-color: #212529;
    }
    .ms-cards{
      .ms-text{
        background-color: #D48F38;
      }
    }    
  }
}


.ms-card{
  width: calc(100% / 5);
}
</style>