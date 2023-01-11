<script>
export default {
  name: 'AppBody'
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
      <div class="flex flex-align-center cursor-pointer">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="Image not found">
        <span>DIGITAL COMICS</span>
      </div>
      <div class="flex flex-align-center cursor-pointer">
        <img src="../assets/img/buy-comics-merchandise.png" alt="Image not found">
        <span>DC MERCHANDISE</span>
      </div>
      <div class="flex flex-align-center cursor-pointer">
        <img src="../assets/img/buy-comics-subscriptions.png" alt="Image not found">
        <span>SUBSCRIPTION</span>
      </div>
      <div class="flex flex-align-center cursor-pointer">
        <img src="../assets/img/buy-comics-shop-locator.png" alt="Image not found">
        <span>COMIC SHOP LOCATOR</span>
      </div>
      <div class="flex flex-align-center cursor-pointer">
        <img src="../assets/img/buy-dc-power-visa.svg" alt="Image not found">
        <span>DC POWER VISA</span>
      </div>
    </div>
  </div>
</template>
<style lang="sass">
  @use '../styles/general' as *
  @use '../styles/partials/variables' as * 
  
  .comic-container
      padding: 2rem 0 

  .shop-container
      padding: 2rem 0 
      background-color: $primary
      .container
        font-size: 13px
        justify-content: space-evenly
      img
        width: 30px
        margin-right: 10px
</style>