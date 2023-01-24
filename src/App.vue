<script>
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import AppMain from './components/AppMain.vue';

export default {
  components:{
    AppHeader,
    AppMain,
    AppFooter
  },
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/generals.scss' as *;
@use './styles/partials/variables' as *;

body{
    background-color: $food-lightgray;
    font-family: 'Catamaran', sans-serif !important;

    a{
      color: $food-black;
    }

    a:hover{
    color: $food-orange;
  }

  .recipe-date{
    color: $food-darkgray;
  }

  .recipe-ico{
    color: $food-orange;
    background-color: $food-white;
    padding: 12px 10px;
    border-radius: 50%;
  }
}
  
</style>