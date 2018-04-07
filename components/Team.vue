<template lang="pug">
  .team
    nuxt-link.team-comp(to='/team/tazhben')
      .team-photo
        img(src='~/assets/img/tazhben.gif')
    nuxt-link.team-comp(to='/team/artem')
      .team-photo
        img(src='~/assets/img/artem.gif')
    nuxt-link.team-comp(to='/team/gosha')
      .team-photo
        img(src='~/assets/img/gosha.gif')
    nuxt-link.team-comp(to='/team/pasha')
      .team-photo
        img(src='~/assets/img/pasha.gif')
        //- span.name Tazhben
        //- p.text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum

</template>
<script>
export default {
  
}
</script>

<style lang="sass" scoped>
.team
  margin-top: 50px
  display: flex
  width: 800px
  justify-content: space-between
  &-photo // на языке sass ==".team-photo"
    width: 150px
    height: 150px
    transition: transform .3s linear
    img
      width: 150px
      height: 250px
    &:hover
      transform: scale(1.2)
      cursor: pointer
  &-body
    width: 150px
    color: #fff
</style>
