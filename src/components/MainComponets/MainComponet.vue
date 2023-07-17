<script></script>
<template>
 <main>
  <div class="container">
    <div class="ms-main-top my-3 px-2">
      <select class="form-select " aria-label="Default select example">
        <option selected>Alien</option>
      </select>
    </div>
    <div class="ms-main-bottom h-100 p-4">
      <div class="ms-header-cards">
        <p class="text-white py-3 px-2 mb-1">Found <span>39</span> cards</p>
      </div>
      <div class="ms-cards row">
        <div class="ms-card col-md-2 mt-0">
          <div class="ms-img-wrapper">
            <img src="../../assets/img/test.png" alt="">
          </div>
          <div class="ms-text text-white text-center fw-bold text-uppercase">
            titolo
            <p class="text-dark fw-normal">tipo</p>
          </div>
        </div>
        <div class="ms-card col-md-2 mt-0">
          <div class="ms-img-wrapper">
            <img src="../../assets/img/test.png" alt="">
          </div>
          <div class="ms-text text-white text-center fw-bold text-uppercase">
            titolo
            <p class="text-dark fw-normal">tipo</p>
          </div>
        </div>
        <div class="ms-card col-md-2 mt-0">
          <div class="ms-img-wrapper">
            <img src="../../assets/img/test.png" alt="">
          </div>
          <div class="ms-text text-white text-center fw-bold text-uppercase">
            titolo
            <p class="text-dark fw-normal">tipo</p>
          </div>
        </div>
        <div class="ms-card col-md-2 mt-0">
          <div class="ms-img-wrapper">
            <img src="../../assets/img/test.png" alt="">
          </div>
          <div class="ms-text text-white text-center fw-bold text-uppercase">
            titolo
            <p class="text-dark fw-normal">tipo</p>
          </div>
        </div>
        <div class="ms-card col-md-2 mt-0">
          <div class="ms-img-wrapper">
            <img src="../../assets/img/test.png" alt="">
          </div>
          <div class="ms-text text-white text-center fw-bold text-uppercase">
            titolo
            <p class="text-dark fw-normal">tipo</p>
          </div>
        </div>
        <div class="ms-card col-md-2 mt-0">
          <div class="ms-img-wrapper">
            <img src="../../assets/img/test.png" alt="">
          </div>
          <div class="ms-text text-white text-center fw-bold text-uppercase">
            titolo
            <p class="text-dark fw-normal">tipo</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  
 </main>
</template>
<style lang="scss" scoped>
main {
  background-color: #D48F38;
  height: 100vh;
  .container{
    height: 100%;
  }
  .form-select{
    max-width: 150px;
  }
  .ms-main-bottom{
    background-color: #fff;
    .ms-header-cards{
      background-color: #212529;
    }
    .ms-cards{
      .ms-card{
        width: calc(100% / 5);
      }
      .ms-text{
        background-color: #D48F38;
      }
    }    
  }
}
</style>