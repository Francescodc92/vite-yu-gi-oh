<script>
  import HeaderComponet from './components/HeaderComponets/HeaderComponet.vue';
  import MainComponet from './components/MainComponets/MainComponet.vue';
  import FooterComponet from './components/FooterComponets/FooterComponet.vue';
  export default{
    components:{
      HeaderComponet,
      MainComponet,
      FooterComponet
    }
  }
</script>

<template>
  <HeaderComponet/>
  <MainComponet/>
  <FooterComponet/>
</template>

<style lang="scss">
@use "./assets/scss/main.scss" as *;
</style>
