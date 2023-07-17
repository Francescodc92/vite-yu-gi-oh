<script>
export default{

  props:{
    cardsArray:{
      type:Array,
      default:[],
    }
  }
}
</script>

<template>

  <div class="col-sm-4 col-md-3 col-lg-2 mx-lg-1 mt-0 flex-column " v-for="(card, index) in cardsArray" :key="index">
    <div class="ms-img-wrapper text-center">
      <img :src="card.card_images[0].image_url" :alt="card.name">
    </div>
    <div class="ms-text text-white text-center fw-bold text-uppercase py-1 px-1">
      {{ card.name }}
      <p class="text-dark fw-normal mt-1">{{ card.archetype }}</p>
    </div>
  </div>

</template>

<style lang="scss" scoped>
.ms-header-cards{
  background-color: #212529;
}

.ms-img-wrapper{
  height:70%;
  img{
    height: 100%;
    width:100%;
    object-fit: fill;
  }
}

.ms-text{
  height: 30%;
  background-color: #D48F38;
  font-size: .875rem;
}
    
</style>