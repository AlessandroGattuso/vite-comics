<script>
  import AppHeader from './components/AppHeader.vue';
  import AppBody from './components/AppBody.vue';
  import AppFooter from './components/AppFooter.vue';

  export default{
    components:{
      AppHeader,
      AppBody,
      AppFooter
    }
  }
</script>

<template>
  <AppHeader></AppHeader>
  <AppBody></AppBody>
  <AppFooter></AppFooter>
</template>

<style lang="sass" scoped>
    // @use './styles/general' as *
    // @use './styles/partials/variables' as * 
    // @use './styles/partials/mixins' as * 
</style>
