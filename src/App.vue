<script>
import AppHeader from './components/AppHeader.vue'

export default {
  components:{
    AppHeader,
  },
}
</script>

<template>
  <AppHeader />
</template>

<style lang="scss">
@use './styles/generals.scss' as *;
@use './styles/partials/variables' as *;

body{
    background-color: $food-lightgray;

    a{
      color: $food-black;
    }

    a:hover{
    color: $food-orange;
}
}
  
</style>