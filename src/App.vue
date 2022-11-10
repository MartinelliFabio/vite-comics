<template>
  
  <HeaderComponent/>
  
  <MainComponent/>
  
  <BlueSectionComponent/>

  <FooterComponent/>

</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import BlueSectionComponent from './components/BlueSectionComponent.vue';
import FooterComponent from './components/FooterComponent.vue';

  export default {
    components: {
      HeaderComponent,
      MainComponent,
      FooterComponent,
      BlueSectionComponent
    }
  }
</script>

<style lang="scss" scoped>

</style>