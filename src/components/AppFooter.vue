<script>
  export default {
      name: 'AppFooter',
      data(){
        return{
          media: [
             'facebook',
             'twitter',
             'youtube',
             'pinterest',
             'periscope'
          ]
        }
      }
  }
</script>
<template>
  <footer>
    <div class="container-fluid dc-background">
      <div class="container flex flex-between text-white">
        <div class="flex lists-container">
          <div>
            <div>
              <h3>DC COMICS</h3>
              <ul>
                <li>Characters</li>
                <li>Comics</li>
                <li>Movies</li>
                <li>Tv</li>
                <li>Games</li>
                <li>Videos</li>
                <li>News</li>
              </ul>
            </div>
            <div>
              <h3>SHOP</h3>
              <ul>
                <li>Shop DC</li>
                <li>Shop DC Collectibles</li>
              </ul>
            </div>
          </div>
          <div>
            <h3>DC</h3>
            <ul>
              <li>Terms Of Use</li>
              <li>Privacy policy(New)</li>
              <li>Ad Choices</li>
              <li>Advertising</li>
              <li>Jobs</li>
              <li>Subscriptions</li>
              <li>Talent Workshop</li>
              <li>CPSC Certificates</li>
              <li>Ratings</li>
              <li>Shop Help</li>
              <li>Contact Us</li>
            </ul>
          </div>
          <div>
            <h3>SITES</h3>
            <ul>
              <li>DC</li>
              <li>MAD Magazine</li>
              <li>DC Kids</li>
              <li>DC Universe</li>
              <li>DC Power Visa</li>
            </ul>
          </div>
        </div>
        <div class="dc-logo-bg">
        </div>
      </div>
    </div>
    <div class="container-fluid bg-lightblack">
        <div class="container flex flex-between">
          <button>SIGN-UP NOW</button>
          <div class="flex media-container">
            <div class="flex flex-align-center">
              <span>FOLLOW US</span>
            </div>
            <div class="flex flex-align-center" v-for="(item, index) in media" :key="index">
              <img :src="`src/assets/img/footer-${item}.png`" alt="Image not found">
            </div>
          </div>
        </div>
    </div>
  </footer>
</template>
<style lang="sass">
    @use '../styles/partials/variables' as *
    @use '../styles/partials/mixins' as *
    @use '../styles/general' as *

    .dc-background
      background: url(src/assets/img/footer-bg.jpg)
      background-repeat: no-repeat
      background-size: auto
    
    ul 
      margin-bottom: .5rem

    li
      line-height: 17px
      font-size: 13px
      color: grey
      &:hover
          cursor: pointer
          color: white

    h3
      font-weight: 600
      margin-bottom: .5rem
    
    .lists-container
      padding: 1.5rem 0
      gap: 20px
    
    .dc-logo-bg
      width: 45%
      background-image: url(src/assets/img/dc-logo-bg.png)
      background-repeat: no-repeat
      background-position-y: 50%
      background-size: cover

    .bg-lightblack
      padding: 1.06rem 0

    .media-container
      font-size: 19px
      gap: 15px
      span
        color: $primary
        font-weight: 600
      img
        width: 25px
        height: 25px
        &:hover
          cursor: pointer
      
    button
      font-size: 17px
      cursor: pointer
      padding: 0.5rem
      color: white
      background-color: transparent
      border: 1.5px solid $primary
      transition: background-color .5s
      &:hover
        background-color: $primary

</style>