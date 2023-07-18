<script>
export default{
  
}
</script>

<template>
 <header>
  <div class="container-fluid d-flex gap-2">
    <div class="img-wrapper">
      <img src="../../assets/img/logo.png" alt="logo yu-gi-ho">
    </div>
    <span>Yu-Gi-oh Api</span>
  </div>
 </header>
</template>


<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
header{
  height: $header-height;
  display: flex;
  align-items: center;
  background-color: #F6F6F6;
  .img-wrapper{
    width: 70px;
  }
  span{
    font-size:1.875rem;
    font-weight: 500;
  }
}
</style>