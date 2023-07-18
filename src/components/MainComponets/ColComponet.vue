<script>
export default{
  props:{
    currentCard:Object
  }
}
</script>

<template>

  <div class="ms-card col-sm-4 col-md-3 col-lg-2 mt-0 d-flex flex-column" >
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
.ms-card{
  cursor:pointer;
  width: 20%;
  .ms-img-wrapper{
    img{
      height: 100%;
      width:100%;
      object-fit: fill;
      transition: transform 200ms ease-in-out;
    }
  }
  &:hover .ms-img-wrapper img{
    transform: scale(1.3);
  }
  .ms-text{
    background-color: #D48F38;
    font-size: .875rem;
  }
}

@media screen and (max-width:992px) {
  .ms-card{
    width: calc(100% / 4);
  }
}

@media screen and (max-width:860px) {
  .ms-card{
    width: calc(100% / 3);
  }
}

@media screen and (max-width:768px) {
  .ms-card{
    width: calc(100% / 2);
  }
}

@media screen and (max-width:576px) {
  .ms-card{
    width:100%;
  }
}

    
</style>