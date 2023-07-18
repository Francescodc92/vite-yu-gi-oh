<script>
import ColComponet from './ColComponet.vue';
import { store } from '../../store.js'
export default{
  data(){
    return {
      store
    }
  },
  components:{
    ColComponet
  },
}
</script>
<template>
 <main>
  <div class="container">
    <div class="ms-main-top py-3 px-2">
      
      <select 
        class="form-select " 
        aria-label="Default select example"
        v-model="store.archetypeSelected"
        @change="$emit('selected')"
      >
        <option value="" selected>All</option>
        <option 
          v-for="(archetype, index) in store.archetypeArray" :key="index"
          :value="archetype.archetype_name"
        >
            {{ archetype.archetype_name }}
        </option>
      </select>
    </div>
    <div class="ms-main-bottom h-100 p-4">
      <div class="ms-header-cards">
        <p class="text-white py-3 px-2 mb-1">Found <span>{{ store.cardsArray.length }}</span> cards</p>
      </div>
      <div class="ms-cards row row-gap-4" v-if="store.cardsArray.length == store.numberRequest">
        <ColComponet v-for="(card, index) in store.cardsArray" :key="index" :currentCard="card"/>
      </div>
      <div class="text-center mt-5" v-else>
        <div class="spinner-border text-primary " role="status">
          <span class="visually-hidden">Loading...</span>
        </div>
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
  }
}
</style>