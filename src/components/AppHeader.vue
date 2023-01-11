<script>
export default {
  name: 'AppHeader',
  data(){
    return{
      menuActive: 1,
      menu: [
          {
            badge: 'characters'
          },
          {
            badge: 'comics'
          },
          {
            badge: 'characters'
          },
          {
            badge: 'movies'
          },
          {
            badge: 'tv'
          },
          {
            badge: 'games'
          },
          {
            badge: 'collectibles'
          },
          {
            badge: 'videos'
          },
          {
            badge: 'fans'
          },
          {
            badge: 'news'
          },
          {
            badge: 'shop'
          }
      ]
    }
  }
}
</script>
<template>
  <header>
    <div class="container flex flex-between flex-align-center h-100">
      <div>
        <img class="logo" src="../assets/img/dc-logo.png" alt="Logo not found">
      </div>
      <div class="menu flex h-100 w-100">
        <ul class="h-100">
          <template v-for="(item, index) in menu" :key="index">
            <li class="h-100 flex flex-center cursor-pointer" :class="(menuActive == index) ? 'active' : ''">
              {{ item.badge }}
            </li>
          </template>
        </ul>
      </div>
    </div>
  </header>
</template>
<style lang="sass" scoped>
  @use '../styles/general' as *
  @use '../styles/partials/variables' as *
  header
    height: 80px
  
  .menu
    justify-content: flex-end
    
  ul
    display: flex
    gap: 20px
    li
      font-size: 11px
      font-weight: 700
      flex-basis: calc(100% / 11)
      text-transform: uppercase
      &:hover,&.active
        color: $primary
      
      &.active
        border-bottom: 5px solid $primary
    
  
  .logo
    height: 55px
    width: 55px
  
</style>