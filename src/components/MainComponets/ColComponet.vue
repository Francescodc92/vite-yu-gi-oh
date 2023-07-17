<script>
export default{
  props:{
    currentCard:Object
  }
}
</script>

<template>

  <div class="col-sm-4 col-md-3 col-lg-2 mx-lg-1 mt-0 flex-grow-1 d-flex flex-column" >
    <div class="ms-img-wrapper text-center">
      <img :src="currentCard.card_images[0].image_url" :alt="currentCard.name">
    </div>
    <div class="ms-text text-white text-center fw-bold text-uppercase py-1 px-1 flex-grow-1">
      {{ currentCard.name }}
      <p class="text-dark fw-normal mt-1">{{ currentCard.archetype }}</p>
    </div>
  </div>

</template>

<style lang="scss" scoped>
.ms-header-cards{
  background-color: #212529;
}

.ms-img-wrapper{
  img{
    height: 100%;
    width:100%;
    object-fit: fill;
  }
}

.ms-text{
  background-color: #D48F38;
  font-size: .875rem;
}
    
</style>