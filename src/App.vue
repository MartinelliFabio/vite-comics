<template>
  
  <HeaderComponent/>

  <JumboComponent/>
  
  <MainComponent/>
  
  <BlueSectionComponent/>

  <FooterComponent/>

</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import JumboComponent from './components/JumboComponent.vue';
import MainComponent from './components/MainComponent.vue';
import BlueSectionComponent from './components/BlueSectionComponent.vue';
import FooterComponent from './components/FooterComponent.vue';

  export default {
    components: {
      HeaderComponent,
      JumboComponent,
      MainComponent,
      FooterComponent,
      BlueSectionComponent
    }
  }
</script>

<style lang="scss" scoped>

</style>