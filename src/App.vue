<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppBlueSection from './components/AppBlueSection.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppBlueSection
  }
}
</script>
<template lang="">
  <div>
    <AppHeader />
    <AppMain />
    <AppBlueSection />
    <AppFooter />
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss' as *;
@use './styles/partials/variables' as *;
</style>