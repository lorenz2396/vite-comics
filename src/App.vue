<script>

import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  components:{
    HeaderComponent,
    MainComponent,
    FooterComponent,
  },
   data(){
      return{

      }
    }
  }
</script>

<template>

<HeaderComponent/>

<MainComponent/>

<FooterComponent/>

</template>

<style lang="scss" >
@use './assets/scss/main' as *;
@use './assets/scss/partials/variables' as *;

header{
  background-color: white;
}

main{
  min-height: 10vh;
  background-color:$content-bg;
}

footer{
  min-height: 60vh;
  background-color: $footer-bg;

}


</style>