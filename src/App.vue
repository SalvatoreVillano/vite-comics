<template>
  <HeaderComponent />
  <MainComponent />
  <SubMain />
  <FooterComponent />
  <SubFooterComponent />
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import SubFooterComponent from './components/SubFooterComponent.vue';
import SubMain from './components/SubMain.vue';

export default {
  components: { HeaderComponent, MainComponent, SubMain, FooterComponent, SubFooterComponent }
}
</script>

<style lang="scss" scoped>

</style>