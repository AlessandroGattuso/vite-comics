<script>
export default {
  name: 'AppBody',
  data(){
    return{
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
  }
}
</script>
<template>
  <div class="container-fluid comic-container bg-black">
    <div class="container flex flex-align-center text-white h-100">
      Content goes here
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
<style lang="sass">
  @use '../styles/general' as *
  @use '../styles/partials/variables' as * 
  @use '../styles/partials/mixins' as * 

  .comic-container
      padding: 2rem 0 

  .shop-container
      padding: 2rem 0 
      background-color: $primary
      .container
        font-size: 13px
        justify-content: space-evenly
        .shop-item
          text-transform: uppercase
      img
        width: 30px
        margin-right: 10px
</style>