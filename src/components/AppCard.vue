<script>
  export default {
    name: 'AppCard',
    props: {
      cardData: Object
    }
  }
</script>
<template>
  <div class="card">
    <img :src="cardData.thumb" alt="Image not found">
    <p class="title">{{ cardData.series }}</p>
  </div>
</template>
<style lang="sass">
  @use '../styles/partials/variables' as *
  @use '../styles/partials/mixins' as *

  .card
    width: calc(100% / 6 - 25px)
  
  img
    width: 100%
    object-fit: cover

  .title
    text-transform: uppercase
</style>