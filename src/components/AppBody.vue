<script>
import AppCard from './AppCard.vue'

export default {
  name: 'AppBody',
  components: {
    AppCard
  },
  data(){
    return{
        cardsData: [],
        shopMenu: [
          {
            label: 'digital comics',
            path: 'src/assets/img/buy-comics-digital-comics.png'
          },
          {
            label: 'dc merchandise',
            path: 'src/assets/img/buy-comics-merchandise.png'
          },
          {
            label: 'subscription',
            path: 'src/assets/img/buy-comics-subscriptions.png'
          },
          {
            label: 'comic shop locator',
            path: 'src/assets/img/buy-comics-shop-locator.png'
          },
          {
            label: 'dc power visa',
            path: 'src/assets/img/buy-dc-power-visa.svg'
          }
        ]
    }
  },
  async mounted() {
    this.cardsData = await (await fetch('src/assets/JSON/dc-comics.json')).json();
  },
}
</script>
<template>
  <div class="container-fluid jumbotron"></div>
  <div class="container-fluid comic-container">
    <div class="container flex flex-align-center text-white h-100">
      <div class="label">
        CURRENT SERIES
      </div>
      <div class="grid-card">
        <AppCard v-for="(card, index) in cardsData" :cardData="card" :key="index"/>
      </div>
    </div>
    <div class="container flex flex-jc-center">
        <button>LOAD MORE</button>
    </div>
  </div>
  <div class="container-fluid shop-container">
    <div class="container flex flex-align-center text-white h-100">
      <div class="flex flex-align-center cursor-pointer shop-item" v-for="(item,index) in shopMenu" :key="index">
        <img :src="item.path" alt="Image not found">
        <span>{{ item.label }}</span>
      </div>
    </div>
  </div>
</template>
<style lang="sass" scoped>
  @use '../styles/partials/variables' as *
  @use '../styles/partials/mixins' as *

  .comic-container
      position: relative
      background-color: $light-dark
      padding: 3rem 0 1.5rem
      .label
        position: absolute
        background-color: $primary
        top: -20px
        left: 150px
        padding: .5rem
        font-size: 22px
        font-weight: 800

      .grid-card
        display: flex
        flex-wrap: wrap
        gap: 30px
        margin-bottom: 2rem

  button
    padding: .5rem 3rem
    color: white
    background-color: $primary
    border: none
    cursor: pointer
    font-size: 16px
    transition: all .5s
    &:hover
      background-color: #2395ff
  .jumbotron
    height: 250px
    background-image: url(src/assets/img/jumbotron.jpg)
    background-size: cover
    background-repeat: no-repeat

  .shop-container
      padding: 2rem 0 
      background-color: $primary
      .container
        font-size: 16px
        justify-content: space-evenly
        .shop-item
          text-transform: uppercase
      img
        width: 30px
        margin-right: 10px
</style>